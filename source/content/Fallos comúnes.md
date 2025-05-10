### 🔌 **Errores de Red y DNS**

1. **FQDNs mal resueltos o sin configurar**:
    
    - `api.<dominio>`, `api-int.<dominio>`, `*.apps.<dominio>` deben resolverse correctamente.
        
    - El nodo bootstrap y los masters deben poder resolver esos nombres internamente.
        
    - ❗ _Solución_: Usa `dnsmasq`, modifica `/etc/hosts`, o configura un DNS interno correctamente.
        
2. **No se puede acceder al registro de imágenes**:
    
    - OKD descarga contenedores desde `quay.io`, y si no hay acceso, la instalación se estanca.
        
    - ❗ _Solución_: Verifica conectividad a Internet o usa un mirror local (más avanzado).
        
3. **Puertos bloqueados entre nodos**:
    
    - El tráfico entre masters (etcd, kubelet, API) debe estar libre.
        
    - ❗ _Solución_: Usa red en modo puente o red NAT bien configurada con todas las VMs en la misma LAN.
        

---

### 🧩 **Errores con Ignition**

1. **Ignition mal configurado o dañado**:
    
    - Si un archivo Ignition no se sirve o se descargó incompleto, el nodo no se configura bien.
        
    - ❗ _Solución_: Verifica los logs de arranque del nodo (`journalctl`) y asegúrate de servir los Ignition por HTTP correctamente.
        
2. **Arranque sin Ignition**:
    
    - A veces el nodo arranca Fedora CoreOS pero no ejecuta Ignition si la imagen fue arrancada sin parámetros adecuados.
        
    - ❗ _Solución_: Asegúrate de pasar la URL del Ignition correctamente en el arranque (kernel args).
        

---

### 🖥️ **Errores de Hardware/VM**

1. **Recursos insuficientes**:
    
    - Bootstrap y master requieren al menos 8–16 GB RAM y 2 CPU cada uno.
        
    - ❗ _Solución_: Ajusta RAM/CPU en las VMs o haz despliegue mínimo (1 master, 0 workers).
        
2. **Disco demasiado pequeño**:
    
    - Fedora CoreOS necesita discos de al menos 120 GB para evitar problemas de instalación de contenedores.
        
    - ❗ _Solución_: Aumenta el disco de las VMs si ves errores relacionados con espacio.
        

---

### 🔐 **Errores de CSR y certificados**

1. **CSRs no aprobados automáticamente**:
    
    - El instalador espera que apruebes las CSRs manualmente cuando no hay automatización.
        
    - ❗ _Solución_: Usa `oc get csr` y `oc adm certificate approve`.
        
2. **Caducidad de certificados**:
    
    - Si repites la instalación varias veces, los certificados previos pueden interferir.
        
    - ❗ _Solución_: Borra el directorio `auth/` o `install-dir/` antes de reiniciar la instalación.
        

---

### ⚠️ **Errores de sincronización o logs vacíos**

1. **No se generan logs en el bootstrap o el master no levanta**:
    
    - Muchas veces debido a un fallo temprano en Ignition.
        
    - ❗ _Solución_: Usa `journalctl -b` desde la VM para rastrear errores de arranque.
        
2. **`kubelet` no existe o falla al arrancar**:
    
    - Aparece si el Ignition no descargó los binarios correctamente.
        
    - ❗ _Solución_: Verifica red y configuración Ignition.
        

---

¿Quieres que te prepare una lista de verificación ("checklist") para antes de lanzar la instalación?