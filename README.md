# trellis-db-push-and-pull
Push and pull databases with trellis and ansible playbooks

## Usage
1. set alias for host files
2. run push or pull playbook `$ ansible-playbook db-push.yml -e "env=ENV site=SITE"`

## Hosts Examples
### 1. Development

```
vagrant 192.168.50.5 ansible_connection=local
[development]
vagrant

[web]
vagrant
```

### 2. Staging

```
production your_server_hostname

[production]
production

[web]
production
```


### 3. Production
```
staging your_server_hostname
[staging]
your_server_hostname

[web]
your_server_hostname
```
