
```
apiVersion: v1
baseDomain: okd.local
metadata:
  name: lab

compute:
- hyperthreading: Enabled
  name: worker
  replicas: 0

controlPlane:
  hyperthreading: Enabled
  name: master
  replicas: 1

networking:
  clusterNetwork:
  - cidr: 10.128.0.0/14 
    hostPrefix: 23 
  networkType: OVNKubernetes
  serviceNetwork: 
  - 172.30.0.0/16

platform:
  none: {}

fips: false

pullSecret: '{"auths":{"cloud.openshift.com":{"auth":"...","email":"..."},"quay.io":{"auth":"...","email":"..."},"registry.connect.redhat.com":{"auth":"...","email":"..."},"registry.redhat.io":{"auth":"...","email":"..."}}}'

sshKey: 'ssh-rsa AAAA...'
```
