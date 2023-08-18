# Ansible playbook and roles to deploy Harbor (Docker Registry)

The *deploy_harbor.yml* playbook uses `install_harbor` and  `prereqs_harbor` roles to install Harbor Registry on a Linux machine (or on Windows if executed on WSL).

As of now, `prereqs_harbor` role only serves to generate SSL certificates with OpenSSL, all its tasks will be skipped if you set `generate_ssl` variable to false in *deploy_harbor.yml*.

To change Harbor configurations not mentioned in *deploy_harbor.yml*, modify the contents of [*harbor.yml.j2*](roles/install_harbor/templates/harbor.yml.j2).

**Prerequisites**:
- Linux terminal
- Docker Engine
- OpenSSL (if you set `generate_ssl` variable to true)