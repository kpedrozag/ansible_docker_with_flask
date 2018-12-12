# Deployment of an API on a Ubuntu docker container using an Ansible playbook

This project explain how to deploy an API built with Flask from a Docker Container of Ubuntu Xenial made from a Dockerfile on another instance (VM) of Ubuntu Xenial by an Ansible playbook.

By clonning the repository from GitHub with `$ git clone https://github.com/kpedrozag/ansible_docker_with_flask.git` and entering to the directory `$ cd ansible_docker_with_flask/`, it can be run the playbook by the command `$ ansible.playbook -i inventory main.yml`.

The file `inventory` has the IP address of the Ubuntu instance. Also, please make sure that the publickey of your local machine is in the authorized_keys file of the Ubuntu instance to the right execution of the playbook.

## Tasks of the playbook

  1. `installation.yml`: This set of tasks make the installation of Docker CE.
  2. `launch_flask.yml`: This tasks download the files to build the image with the API and run an instance of the created image.
  3. `remove.yml`: This tasks uninstall Docker CE from the Ubuntu instance.