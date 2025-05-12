# Guía de instalación de OKD4

> [!Warning]
> En desarrollo...

Empezar por aquí: [[1. Instalación utilidades services]]
![[Diseño lógico red ODAP-Página-2.drawio.png]]

| nombre            | ram(GB) | cpu(logic CPU) | disco(GB) |
| ----------------- | ------- | -------------- | --------- |
| **IZQ**           |         |                |           |
| router IZQ        | 1       | 2              | 20        |
| Bootstrap-worker1 | 16      | 4              | 120       |
| Services          | 10      | 4              | 120       |
| Master            | 16      | 4              | 120       |
| **DER**           |         |                |           |
| router DER        | 1       | 2              | 20        |
| worker2           |         |                |           |

> [!abstract] Guías recomendadas en las que se basa esta guía
> - https://itnext.io/guide-installing-an-okd-4-5-cluster-508a2631cbee        
> - https://labrepo.com/openshift-4-okd-bare-metal-install-on-vmware-homelab/     
> - https://computingforgeeks.com/deploy-multi-node-okd-cluster-using-fedora-coreos/ 
> - https://github.com/eduardolucioac/okd_bare_metal

> [!INFO] Esta pagina se desplegó usando esta guía
>  - https://dev.to/defenderofbasic/host-your-obsidian-notebook-on-github-pages-for-free-8l1
