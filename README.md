# trellis-db-push-and-pull
Push and pull databases with trellis and ansible playbooks

## Usage
1. set alias for host files
2. run push or pull playbook `$ ansible-playbook db-push.yml -e "env=ENV site=SITE"`

## Hosts Examples
### 1. Development

```
vagrant 192.168.50.5 ansible_connection=ssh ansible_user=vagrant ansible_user=vagrant ansible_ssh_private_key_file=.vagrant/machines/default/virtualbox/private_key
[development]
vagrant

[web]
vagrant
```

### 2. Staging

```
staging your_server_hostname

[staging]
staging

[web]
staging
```


### 3. Production
```
production your_server_hostname
[production]
production

[web]
production
```
