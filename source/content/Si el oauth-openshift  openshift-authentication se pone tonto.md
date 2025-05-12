> Warning FailedScheduling 34m default-scheduler 0/2 nodes are available: 1 node(s) didn't match Pod's node affinity/selector, 1 node(s) didn't match pod anti-affinity rules. preemption: 0/2 nodes are available: 1 Preemption is not helpful for scheduling, 1 node(s) didn't match pod anti-affinity rules.

```
oc edit deployment oauth-openshift -n openshift-authentication
```

Se cambia ``requiredDuringSchedulingIgnoredDuringExecution:`` por ``preferredDuringSchedulingIgnoredDuringExecution:`` y se añade el weight. 

> [!abstract] Creo que pasa por tener 1 solo worker, poniendo 2 al menos igual arreglas.
>

```
podAntiAffinity:
          preferredDuringSchedulingIgnoredDuringExecution:
            - weight: 100
              podAffinityTerm:
                labelSelector:
                  matchLabels:
                    app: oauth-openshift
                    oauth-openshift-anti-affinity: "true"
                topologyKey: kubernetes.io/hostname
```