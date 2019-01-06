# workstation-hieradata

To use this config:


Mac (bash):
```
sudo gem install puppet --no-ri --no-doc; \
sudo puppet module install call-workstation; \
curl -L https://github.com/call/workstation-hieradata/archive/master.zip | \
    bsdtar -xvf - -C ~; \
sudo puppet apply -e "class {'workstation': user => $(whoami)}" \
    --hiera_config ~/workstation-hieradata-master/hiera.yaml
```

Linux (bash):
```
sudo gem install puppet --no-ri --no-doc; \
sudo puppet module install call-workstation; \
cd ~; git clone https://github.com/call/workstation-hieradata.git; \
sudo puppet apply -e "class {'workstation': user => $(whoami)}" \
    --hiera_config ~/workstation-hieradata/hiera.yaml
```