Si al hacer ``oc describe pods -n openshift-authenticationoauth-openshift 

`Warning FailedScheduling 34m default-scheduler 0/2 nodes are available: 1 node(s) didn't match Pod's node affinity/selector, 1 node(s) didn't match pod anti-affinity rules. preemption: 0/2 nodes are available: 1 Preemption is not helpful for scheduling, 1 node(s) didn't match pod anti-affinity rules.`

```
oc edit deployment oauth-openshift -n openshift-authentication
```

Buscar donde incrustar esto en el yaml respetando la estructura y guardar:

```
spec:
  nodePlacement:
    nodeSelector:
      matchLabels:
        node-role.kubernetes.io/worker: ""
```

Los cambios se gestionan solos y cuando reinicie el pod el router debería desplegarse exitosamente. 
