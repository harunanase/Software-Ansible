# Software Ansible

A collection of installing various softwares using Ansible

## Pre-requires

1. Ansible

## Usage

1. Edit `inventory/dev.yml` to config your hosts
2. Execute `ansible-playbook playbooks/ping.yml --limit _YOUR_HOST_`
to check the connection (you should substitute the variable `_YOUR_HOST_`).
3. Execute `ansbile-playbook playbooks/install_XXX.yml --limit _YOUR_HOST_`
to install your desire software.

## Current support software

1. docker and docker-compose

## Config Options

- You can config the software versions, install path, ... etc. at the file `playbooks/roles/_SOFTWARE_ansible_/defaults/main.yml`
- For example, the docker config file is at `playbooks/roles/docker_ansible/defaults/main.yml`
