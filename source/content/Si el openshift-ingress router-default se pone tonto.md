>Warning FailedScheduling 73m (x4 over 88m) default-scheduler 0/1 nodes are available: 1 node(s) had untolerated taint {node-role.kubernetes.io/master: }. preemption: 0/1 nodes are available: 1 Preemption is not helpful for scheduling.

Esto abre un yaml en vim:

```
oc edit ingresscontroller default -n openshift-ingress-operator
```

Buscar donde incrustar esto en el yaml respetando la estructura y guardar:

```
spec:
  nodePlacement:
    tolerations:
    - key: "node-role.kubernetes.io/master"
      operator: "Exists"
      effect: "NoSchedule"
```

Los cambios se gestionan solos
