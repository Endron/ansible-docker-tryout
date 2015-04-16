# ansible-docker-tryout

Some experimenting on using Ansible to change the container running on a docker host.
- The docker host is created using Vagrant.
- Then Ansible is used to deploy a version of jenkins (playbook = deploy-app.yml)
- Then Ansible is run again, to replace the deployed jenkins container with a new version (playbook = deploy-app-2.yml)

## Lessons Learned
- Replacing containers only works correctly when the container name is specifiyed in the playbook
- Sepecifying a name does not work with setting a count of containers
