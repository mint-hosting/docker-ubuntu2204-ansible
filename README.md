# Ubuntu 22.04 LTS (Jammy Jellyfish) Ansible Docker image

![example workflow](https://github.com/mint-hosting/docker-ubuntu2204-ansible/actions/workflows/build.yml/badge.svg)


Ubuntu 22.04 LTS (Jammy Jellyfish) Docker container for Ansible playbook and role testing.

## How to Build

This image is built on ghcr.io automatically any time the official OS container is rebuilt, and any time a commit is made or merged to the `master` branch. But if you need to build the image on your own locally, do the following:

  1. [Install Docker](https://docs.docker.com/install/).
  2. `cd` into this directory.
  3. Run `docker build -t ubuntu2204-ansible .`

## How to Use

  1. [Install Docker](https://docs.docker.com/engine/installation/).
  2. Pull this image from ghcr.io: `docker pull ghcr.io/mint-hosting/docker-ubuntu2204-ansible/docker-ubuntu2204-ansible:latest`
  3. Run a container from the image: `docker run --detach --privileged ghcr.io/mint-hosting/docker-ubuntu2204-ansible/docker-ubuntu2204-ansible:latest`
  4. Use Ansible inside the container:  
    a. `docker exec --tty [container_id] env TERM=xterm ansible --version`  
    b. `docker exec --tty [container_id] env TERM=xterm ansible-playbook /path/to/ansible/playbook.yml --syntax-check`  

## Notes

This container image allow us to test Ansible playbooks and roles with Molecule framework.

## Author

Created in 2023. by Petar Kozic petar.kozic@mint.rs