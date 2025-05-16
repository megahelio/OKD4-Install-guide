[root@apps opt]# openshift-install --dir=install_dir/ wait-for bootstrap-complete --log-level=info

> INFO Waiting up to 20m0s (until 11:42AM CEST) for the Kubernetes API at https://api.lab.okd.local:6443...
> INFO API v1.30.6-dirty up
> INFO Waiting up to 45m0s (until 12:18PM CEST) for bootstrapping to complete...
> INFO Cluster operator cloud-controller-manager TrustedCABundleControllerControllerAvailable is True with AsExpected: Trusted CA Bundle Controller works as expected
> INFO Cluster operator cloud-controller-manager TrustedCABundleControllerControllerDegraded is False with AsExpected: Trusted CA Bundle Controller works as expected
> INFO Cluster operator cloud-controller-manager CloudConfigControllerAvailable is True with AsExpected: Cloud Config Controller works as expected
> INFO Cluster operator cloud-controller-manager CloudConfigControllerDegraded is False with AsExpected: Cloud Config Controller works as expected
> INFO Cluster operator network ManagementStateDegraded is False with :
> INFO Cluster operator network Progressing is True with Deploying: DaemonSet "/openshift-multus/network-metrics-daemon" is waiting for other operators to become ready
> INFO DaemonSet "/openshift-network-operator/iptables-alerter" is waiting for other operators to become ready
> INFO Deployment "/openshift-multus/multus-admission-controller" is waiting for other operators to become ready
> INFO Use the following commands to gather logs from the cluster
> INFO openshift-install gather bootstrap --help
> ERROR Bootstrap failed to complete: timed out waiting for the condition
> ERROR Failed to wait for bootstrapping to complete. This error usually happens when there is a problem with control plane hosts that prevents the control plane operators from creating the control plane.


[root@apps opt]# oc get clusteroperators
NAME                                       VERSION             AVAILABLE   PROGRESSING   DEGRADED   SINCE   MESSAGE
authentication                             4.18.0-okd-scos.9   False       False         True       11h     APIServicesAvailable: PreconditionNotReady...
baremetal                                  4.18.0-okd-scos.9   True        False         False      11h
cloud-controller-manager                   4.18.0-okd-scos.9   True        False         False      11h
cloud-credential                           4.18.0-okd-scos.9   True        False         False      11h
cluster-autoscaler                         4.18.0-okd-scos.9   True        False         False      11h
config-operator                            4.18.0-okd-scos.9   True        False         False      11h
console
control-plane-machine-set                  4.18.0-okd-scos.9   True        False         False      11h
csi-snapshot-controller                    4.18.0-okd-scos.9   True        False         False      11h
dns                                        4.18.0-okd-scos.9   True        False         False      11h
etcd                                                           False       True          True       11h     StaticPodsAvailable: 0 nodes are active; 1 node is at revision 0; 0 nodes have achieved new revision 1
image-registry
ingress                                    4.18.0-okd-scos.9   True        True          False      11h     ingresscontroller "default" is progressing: IngressControllerProgressing: One or more status conditions indicate progressing: DeploymentRollingOut=True (DeploymentRollingOut: Waiting for router deployment rollout to finish: 0 of 1 updated replica(s) are available......
insights                                   4.18.0-okd-scos.9   True        False         False      11h
kube-apiserver                                                 False       True          True       11h     StaticPodsAvailable: 0 nodes are active; 1 node is at revision 0; 0 nodes have achieved new revision 3
kube-controller-manager                                        False       True          True       11h     StaticPodsAvailable: 0 nodes are active; 1 node is at revision 0; 0 nodes have achieved new revision 3
kube-scheduler                                                 False       True          True       11h     StaticPodsAvailable: 0 nodes are active; 1 node is at revision 0; 0 nodes have achieved new revision 5
kube-storage-version-migrator              4.18.0-okd-scos.9   True        False         False      11h
machine-api                                4.18.0-okd-scos.9   True        False         False      11h
machine-approver                           4.18.0-okd-scos.9   True        False         False      11h
machine-config                                                 True        True          True       11h     Unable to apply 4.18.0-okd-scos.9: error during syncRequiredMachineConfigPools: [context deadline exceeded, MachineConfigPool master has not progressed to latest configuration: configuration status for pool master is empty: 0 (ready 0) out of 1 nodes are updating to latest configuration rendered-master-2f2b24594582bd440c90e8a5b0d48c2c, retrying]
marketplace                                4.18.0-okd-scos.9   True        False         False      11h
monitoring                                                     False       True          True       11h     UpdatingPrometheusOperator: reconciling Prometheus Operator Admission Webhook Deployment failed: updating Deployment object failed: waiting for DeploymentRollout of openshift-monitoring/prometheus-operator-admission-webhook: context deadline exceeded: got 1 unavailable replicas
network                                    4.18.0-okd-scos.9   True        True          False      11h     DaemonSet "/openshift-multus/network-metrics-daemon" is waiting for other operators to become ready...
node-tuning                                4.18.0-okd-scos.9   True        False         False      11h
olm                                        4.18.0-okd-scos.9   False       True          True       11h     CatalogdDeploymentCatalogdControllerManagerAvailable: Waiting for Deployment...
openshift-apiserver                        4.18.0-okd-scos.9   False       False         False      11h     APIServicesAvailable: PreconditionNotReady
openshift-controller-manager               4.18.0-okd-scos.9   True        False         False      11h
openshift-samples
operator-lifecycle-manager                 4.18.0-okd-scos.9   True        False         False      11h
operator-lifecycle-manager-catalog         4.18.0-okd-scos.9   True        False         False      11h
operator-lifecycle-manager-packageserver                       False       False         False      11h     ClusterServiceVersion openshift-operator-lifecycle-manager/packageserver observed in phase Failed with reason: InstallCheckFailed, message: install timeout
service-ca                                 4.18.0-okd-scos.9   True        False         False      11h
storage                                    4.18.0-okd-scos.9   True        False         False      11h
[root@apps opt]# oc describe nodes | more
Name:               okd4-control-plane-1.lab.okd.local
Roles:              control-plane,master
Labels:             beta.kubernetes.io/arch=amd64
                    beta.kubernetes.io/os=linux
                    kubernetes.io/arch=amd64
                    kubernetes.io/hostname=okd4-control-plane-1.lab.okd.local
                    kubernetes.io/os=linux
                    node-role.kubernetes.io/control-plane=
                    node-role.kubernetes.io/master=
                    node.openshift.io/os_id=scos
Annotations:        k8s.ovn.org/host-cidrs: ["192.168.112.103/24"]
                    k8s.ovn.org/l3-gateway-config:
                      {"default":{"mode":"shared","bridge-id":"br-ex","interface-id":"br-ex_okd4-control-plane-1.lab.okd.local","mac-address":"00:0c:29:c4:6
6:56...
                    k8s.ovn.org/network-ids: {"default":"0"}
                    k8s.ovn.org/node-chassis-id: 437052ed-1444-4311-ac38-92e36417d109
                    k8s.ovn.org/node-gateway-router-lrp-ifaddrs: {"default":{"ipv4":"100.64.0.2/16"}}
                    k8s.ovn.org/node-id: 2
                    k8s.ovn.org/node-masquerade-subnet: {"ipv4":"169.254.0.0/17","ipv6":"fd69::/112"}
                    k8s.ovn.org/node-primary-ifaddr: {"ipv4":"192.168.112.103/24"}
                    k8s.ovn.org/node-subnets: {"default":["10.128.0.0/23"]}
                    k8s.ovn.org/node-transit-switch-port-ifaddr: {"ipv4":"100.88.0.2/16"}
                    k8s.ovn.org/remote-zone-migrated: okd4-control-plane-1.lab.okd.local
                    k8s.ovn.org/zone-name: okd4-control-plane-1.lab.okd.local
                    machineconfiguration.openshift.io/controlPlaneTopology: SingleReplica
                    volumes.kubernetes.io/controller-managed-attach-detach: true
CreationTimestamp:  Tue, 06 May 2025 00:52:00 +0200
Taints:             node-role.kubernetes.io/master:NoSchedule
                    UpdateInProgress:PreferNoSchedule
Unschedulable:      false
Lease:
  HolderIdentity:  okd4-control-plane-1.lab.okd.local
  AcquireTime:     <unset>
  RenewTime:       Tue, 06 May 2025 12:16:59 +0200
Conditions:
  Type             Status  LastHeartbeatTime                 LastTransitionTime                Reason                       Message
  ----             ------  -----------------                 ------------------                ------                       -------
  MemoryPressure   False   Tue, 06 May 2025 01:59:25 +0200   Tue, 06 May 2025 00:52:00 +0200   KubeletHasSufficientMemory   kubelet has sufficient memory av
ailable
  DiskPressure     False   Tue, 06 May 2025 01:59:25 +0200   Tue, 06 May 2025 00:52:00 +0200   KubeletHasNoDiskPressure     kubelet has no disk pressure
  PIDPressure      False   Tue, 06 May 2025 01:59:25 +0200   Tue, 06 May 2025 00:52:00 +0200   KubeletHasSufficientPID      kubelet has sufficient PID avail
able
  Ready            True    Tue, 06 May 2025 01:59:25 +0200   Tue, 06 May 2025 00:54:02 +0200   KubeletReady                 kubelet is posting ready status
Addresses:
  InternalIP:  192.168.112.103
  Hostname:    okd4-control-plane-1.lab.okd.local
Capacity:
  cpu:                2
  ephemeral-storage:  51837932Ki
  hugepages-1Gi:      0
  hugepages-2Mi:      0
  memory:             7949420Ki
  pods:               250
Allocatable:
  cpu:                1500m
  ephemeral-storage:  46700096229
  hugepages-1Gi:      0
  hugepages-2Mi:      0
  memory:             6798444Ki
  pods:               250
System Info:
  Machine ID:                                       d9d3c9629b524317ad6e6ccaafd699e6
  System UUID:                                      b0f84d56-6b8f-a0fa-ba07-0bc43af7fd7e
  Boot ID:                                          94742383-8096-49bc-b8ce-5ee01be6c29c
  Kernel Version:                                   5.14.0-580.el9.x86_64
  OS Image:                                         CentOS Stream CoreOS 418.9.202504250632-0
  Operating System:                                 linux
  Architecture:                                     amd64
  Container Runtime Version:                        cri-o://1.31.6
  Kubelet Version:                                  v1.31.7
  Kube-Proxy Version:                               v1.31.7
Non-terminated Pods:                                (59 in total)
  Namespace                                         Name                                                          CPU Requests  CPU Limits  Memory Requests
 Memory Limits  Age
  ---------                                         ----                                                          ------------  ----------  ---------------
 -------------  ---
  openshift-apiserver-operator                      openshift-apiserver-operator-756f964595-2f94w                 10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         65m
  openshift-apiserver                               apiserver-d5dc9c7bb-72q2z                                     110m (7%)     0 (0%)      250Mi (3%)
 0 (0%)         67m
  openshift-authentication-operator                 authentication-operator-7ff884db8f-dp4vk                      20m (1%)      0 (0%)      200Mi (3%)
 0 (0%)         63m
  openshift-catalogd                                catalogd-controller-manager-7f5dd586f7-f9pmt                  105m (7%)     0 (0%)      264Mi (3%)
 0 (0%)         66m
  openshift-cloud-controller-manager-operator       cluster-cloud-controller-manager-operator-599d6b6579-ttmx2    30m (2%)      0 (0%)      95Mi (1%)
 0 (0%)         69m
  openshift-cloud-credential-operator               cloud-credential-operator-78665fcb6c-7pxsv                    20m (1%)      0 (0%)      40Mi (0%)
 0 (0%)         66m
  openshift-cluster-machine-approver                machine-approver-794479b9b-rnd49                              20m (1%)      0 (0%)      70Mi (1%)
 0 (0%)         66m
  openshift-cluster-node-tuning-operator            cluster-node-tuning-operator-6646dfbf76-d855s                 10m (0%)      0 (0%)      20Mi (0%)
 0 (0%)         63m
  openshift-cluster-node-tuning-operator            tuned-x496p                                                   10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         66m
  openshift-cluster-olm-operator                    cluster-olm-operator-7c5f4fc85c-rpfcc                         10m (0%)      0 (0%)      20Mi (0%)
 0 (0%)         63m
  openshift-cluster-samples-operator                cluster-samples-operator-b8c9f975c-vd5t4                      20m (1%)      0 (0%)      100Mi (1%)
 0 (0%)         63m
  openshift-cluster-storage-operator                cluster-storage-operator-869fffd44-98c4p                      10m (0%)      0 (0%)      20Mi (0%)
 0 (0%)         63m
  openshift-cluster-storage-operator                csi-snapshot-controller-868779b868-mlph7                      10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         65m
  openshift-cluster-storage-operator                csi-snapshot-controller-operator-84c4d496b8-blfcb             10m (0%)      0 (0%)      65Mi (0%)
 0 (0%)         65m
  openshift-cluster-version                         cluster-version-operator-7f66c6c794-zt9g9                     20m (1%)      0 (0%)      50Mi (0%)
 0 (0%)         66m
  openshift-config-operator                         openshift-config-operator-5b4f6b6f9c-66m6c                    10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         65m
  openshift-controller-manager-operator             openshift-controller-manager-operator-655757cf65-kjqn5        10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         63m
  openshift-controller-manager                      controller-manager-6cc58b895f-9tx7d                           100m (6%)     0 (0%)      100Mi (1%)
 0 (0%)         66m
  openshift-dns-operator                            dns-operator-78694f5b5d-x7xbc                                 20m (1%)      0 (0%)      69Mi (1%)
 0 (0%)         66m
  openshift-dns                                     dns-default-sbs44                                             60m (4%)      0 (0%)      110Mi (1%)
 0 (0%)         62m
  openshift-dns                                     node-resolver-c24sk                                           5m (0%)       0 (0%)      21Mi (0%)
 0 (0%)         62m
  openshift-etcd-operator                           etcd-operator-5d477bcddb-rmfp2                                10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         63m
  openshift-image-registry                          cluster-image-registry-operator-64b5b5bd58-sjtsq              10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         65m
  openshift-ingress-operator                        ingress-operator-79c94b4f5b-6br4w                             20m (1%)      0 (0%)      96Mi (1%)
 0 (0%)         63m
  openshift-insights                                insights-operator-58f6654c7c-sjtz6                            10m (0%)      0 (0%)      54Mi (0%)
 0 (0%)         69m
  openshift-kube-apiserver-operator                 kube-apiserver-operator-7455ff747c-m6b8v                      10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         63m
  openshift-kube-controller-manager-operator        kube-controller-manager-operator-cd8558744-grzzt              10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         65m
  openshift-kube-scheduler-operator                 openshift-kube-scheduler-operator-78f9b79f47-dccjc            10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         65m
  openshift-kube-storage-version-migrator-operator  kube-storage-version-migrator-operator-5779c5cfc7-6ngnc       10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         63m
  openshift-kube-storage-version-migrator           migrator-5c4cc79cbf-gb4pl                                     11m (0%)      0 (0%)      201Mi (3%)
 0 (0%)         63m
  openshift-machine-api                             cluster-autoscaler-operator-856b47f9c8-z6m7f                  30m (2%)      0 (0%)      70Mi (1%)
 0 (0%)         70m
  openshift-machine-api                             cluster-baremetal-operator-5577fc8679-xvkw7                   20m (1%)      0 (0%)      70Mi (1%)
 0 (0%)         69m
  openshift-machine-api                             control-plane-machine-set-operator-cc9787d7c-cncn4            10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         65m
  openshift-machine-api                             machine-api-operator-7d8cbb76d7-98hn2                         20m (1%)      0 (0%)      70Mi (1%)
 0 (0%)         69m
  openshift-machine-config-operator                 kube-rbac-proxy-crio-okd4-control-plane-1.lab.okd.local       20m (1%)      0 (0%)      50Mi (0%)
 0 (0%)         70m
  openshift-machine-config-operator                 machine-config-controller-6f84bdd8b6-ltxs8                    40m (2%)      0 (0%)      100Mi (1%)
 0 (0%)         62m
  openshift-machine-config-operator                 machine-config-daemon-xc87f                                   40m (2%)      0 (0%)      100Mi (1%)
 0 (0%)         62m
  openshift-machine-config-operator                 machine-config-operator-796457cf68-fcnjn                      40m (2%)      0 (0%)      100Mi (1%)
 0 (0%)         66m
  openshift-machine-config-operator                 machine-config-server-6dp6b                                   20m (1%)      0 (0%)      50Mi (0%)
 0 (0%)         62m
  openshift-marketplace                             community-operators-7vbn4                                     10m (0%)      0 (0%)      120Mi (1%)
 0 (0%)         64m
  openshift-marketplace                             community-operators-ktjbl                                     10m (0%)      0 (0%)      120Mi (1%)
 0 (0%)         <invalid>
  openshift-marketplace                             marketplace-operator-88655d5d4-xngvs                          1m (0%)       0 (0%)      5Mi (0%)
 0 (0%)         63m
  openshift-monitoring                              cluster-monitoring-operator-556c697f8-5pnsh                   10m (0%)      0 (0%)      75Mi (1%)
 0 (0%)         65m
  openshift-multus                                  multus-additional-cni-plugins-tx8hn                           10m (0%)      0 (0%)      10Mi (0%)
 0 (0%)         69m
  openshift-multus                                  multus-admission-controller-7dd7d55cc6-srlvb                  20m (1%)      0 (0%)      70Mi (1%)
 0 (0%)         63m
  openshift-multus                                  multus-n4jsn                                                  10m (0%)      0 (0%)      65Mi (0%)
 0 (0%)         69m
  openshift-network-node-identity                   network-node-identity-x7pbt                                   20m (1%)      0 (0%)      100Mi (1%)
 0 (0%)         69m
  openshift-network-operator                        network-operator-6c8c667c44-9hppp                             10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         70m
  openshift-oauth-apiserver                         apiserver-747f5fd8ff-h6vvt                                    150m (10%)    0 (0%)      200Mi (3%)
 0 (0%)         67m
  openshift-operator-controller                     operator-controller-controller-manager-7f7b74ffc7-nnvvh       15m (1%)      0 (0%)      128Mi (1%)
 0 (0%)         66m
  openshift-operator-lifecycle-manager              catalog-operator-ddc99d56b-rtvwp                              10m (0%)      0 (0%)      80Mi (1%)
 0 (0%)         65m
  openshift-operator-lifecycle-manager              olm-operator-b65bbf5c4-6kb8w                                  10m (0%)      0 (0%)      160Mi (2%)
 0 (0%)         65m
  openshift-operator-lifecycle-manager              package-server-manager-9db885b9-vx6fq                         20m (1%)      0 (0%)      30Mi (0%)
 0 (0%)         66m
  openshift-operator-lifecycle-manager              packageserver-6c95d6c764-nn9kd                                10m (0%)      0 (0%)      50Mi (0%)
 0 (0%)         66m
  openshift-ovn-kubernetes                          ovnkube-control-plane-bd8bfc487-b9tt4                         20m (1%)      0 (0%)      320Mi (4%)
 0 (0%)         63m
  openshift-ovn-kubernetes                          ovnkube-node-6tcxv                                            80m (5%)      0 (0%)      1630Mi (24%)
 0 (0%)         68m
  openshift-route-controller-manager                route-controller-manager-5c488bf647-9t6jm                     100m (6%)     0 (0%)      100Mi (1%)
 0 (0%)         66m
  openshift-service-ca-operator                     service-ca-operator-79cb494bb4-22g9c                          10m (0%)      0 (0%)      80Mi (1%)
 0 (0%)         65m
  openshift-service-ca                              service-ca-76564f9658-27dqh                                   10m (0%)      0 (0%)      120Mi (1%)
 0 (0%)         65m
Allocated resources:
  (Total limits may be over 100 percent, i.e., overcommitted.)
  Resource           Requests      Limits
  --------           --------      ------
  cpu                1497m (99%)   0 (0%)
  memory             6568Mi (98%)  0 (0%)
  ephemeral-storage  0 (0%)        0 (0%)
  hugepages-1Gi      0 (0%)        0 (0%)
  hugepages-2Mi      0 (0%)        0 (0%)
Events:
  Type    Reason          Age   From             Message
  ----    ------          ----  ----             -------
  Normal  RegisteredNode  70m   node-controller  Node okd4-control-plane-1.lab.okd.local event: Registered Node okd4-control-plane-1.lab.okd.local in Controller
  Normal  RegisteredNode  52m   node-controller  Node okd4-control-plane-1.lab.okd.local event: Registered Node okd4-control-plane-1.lab.okd.local in Controller
  Normal  RegisteredNode  32m   node-controller  Node okd4-control-plane-1.lab.okd.local event: Registered Node okd4-control-plane-1.lab.okd.local in Controller
  Normal  RegisteredNode  11m   node-controller  Node okd4-control-plane-1.lab.okd.local event: Registered Node okd4-control-plane-1.lab.okd.local in Controller