```
openshift-install create manifests --dir=install_dir/
sed -i 's/mastersSchedulable: true/mastersSchedulable: False/' install_dir/manifests/cluster-scheduler-02-config.yml
openshift-install create ignition-configs --dir=install_dir/
sudo cp -R install_dir/* /var/www/html/okd4/ 
sudo chown -R apache: /var/www/html/ 
sudo chmod -R 755 /var/www/html/
```

```
sudo wget https://builds.coreos.fedoraproject.org/prod/streams/stable/builds/42.20250410.3.1/x86_64/fedora-coreos-42.20250410.3.1-metal.x86_64.raw.xz
sudo wget https://builds.coreos.fedoraproject.org/prod/streams/stable/builds/42.20250410.3.1/x86_64/fedora-coreos-42.20250410.3.1-metal.x86_64.raw.xz.sig
 
sudo mv fedora-coreos-42.20250410.3.1-metal.x86_64.raw.xz fcos.raw.xz
sudo mv fedora-coreos-42.20250410.3.1-metal.x86_64.raw.xz.sig fcos.raw.xz.sig
 
sudo chown -R apache: /var/www/html/
sudo chmod -R 755 /var/www/html/

coreos.inst.install_dev=/dev/nvme0n1
coreos.inst.image_url=http://192.168.112.102:8080/okd4/fcos.raw.xz
coreos.inst.ignition_url=http://192.168.112.102:8080/okd4/bootstrap.ign
```