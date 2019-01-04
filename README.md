# workstation-hieradata

To use this config:

```
sudo gem install puppet --no-ri --no-doc; \
sudo puppet module install call-workstation; \ 

curl -L https://github.com/call/workstation-hieradata/archive/master.zip | \
    bsdtar -xvf - -C ~; \

sudo puppet apply -e "include workstation" \
    --hiera_config ~/workstation-hieradata-master/hiera.yaml
```
