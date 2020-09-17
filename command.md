# Useful commands through the course

## Execute a git command on all hosts

ansible -m command -a "git config --global --list"  -u azureuser all

## Execute a git command on all hosts with maximum verbosity

ansible -m command -a "git config --global --list"  -u azureuser -vvv --check all

## Execute a git command on all hosts with minimum verbosity and check only

ansible -m command -a "git config --global --list"  -u azureuser -v --check all

## Check for a package manager ona host

ansible -m setup -a "filter=ansible_pkg_mgr" -u azureuser all

## Run a playbook 

ansible-playbook playbook-git.yml -u azureuser

## Run a docker image to install Ansible and play with ansible-console

docker run --rm -it python bash

## Connect to a container named ansible_container_test1 and start bash

docker container exec -it ansible_container_test1 bash
