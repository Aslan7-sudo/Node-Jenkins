# Docker on Ubuntu 20.04

This playbook will install Docker an Ubuntu 20.04
A number of containers will be created with the options specified in the `vars/default.yml` variable file.

## Settings

- `create_containers`: number of containers to create.
- `default_container_name`: default name for new containers.
- `default_container_image`: default image for new containers.
- `default_container_command`: default command to run on new containers.


## Running this Playbook

Quick Steps:

### 1. Obtain the playbook
```shell
git clone https://github.com/snjksh82/Ansible_AWS.git
cd Ansible_AWS/playbooks/docker_ubuntu2004
```

### 2. Customize Options

```shell
vi vars/default.yml
```

```yml
#vars/default.yml
---
create_containers: 3
default_container_name: docker_created_by_ansible
default_container_image: ubuntu
default_container_command: sleep 1d
```

### 3. Run the Playbook

```command
ansible-playbook playbook.yml -l [target] --private-key [.pem] -u [remote user] 
