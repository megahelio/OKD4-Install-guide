
```
#!/bin/bash
sudo rm -r install_dir/
mkdir install_dir/
cp install-config.yaml.bak ./install_dir/install-config.yaml
openshift-install create manifests --dir=install_dir/
sed -i 's/mastersSchedulable: true/mastersSchedulable: False/' install_dir/manifests/cluster-scheduler-02-config.yml
openshift-install create ignition-configs --dir=install_dir/

sudo rm -r /var/www/html/okd4
sudo mkdir /var/www/html/okd4
sudo cp -R install_dir/* /var/www/html/okd4/
sudo chown -R apache: /var/www/html/
sudo chmod -R 755 /var/www/html/
openshift-install --dir=install_dir/ wait-for bootstrap-complete --log-level=debug
```
