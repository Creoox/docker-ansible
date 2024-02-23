# Ansible

Ansible inside Docker for consistent running of ansible inside your local machine or CI/CD system. You can view [CHANGELOG](https://github.com/willhallonline/docker-ansible/blob/master/CHANGELOG.md) to understand what changes have happened to this recently.

[![Docker Pulls](https://img.shields.io/docker/pulls/willhallonline/ansible.svg "Docker Pulls")][hub] ![Docker Image Size (tag)](https://img.shields.io/docker/image-size/willhallonline/ansible/latest)

## Current Ansible Core Versions

These are the latest Ansible Core versions running within the containers:

- Ansible 2.9: 2.9.27
- Ansible 2.10: 2.10.17
- Ansible 2.11: 2.11.12
- Ansible 2.12: 2.12.10
- Ansible 2.13: 2.13.13
- Ansible 2.14: 2.14.14
- Ansible 2.15: 2.15.9
- Ansible 2.16: 2.16.3

### Compatibility

- Currently, Ansible 2.12+ is not working on Centos 7, Centos 8, Rocky Linux 8, Debian Stretch, Debian Buster or Ubuntu 18.04 due to dependency on Python 3.8+.
- Currently, Ansible 2.13+ is not working on Ubuntu 20.04 due to dependency on Python 3.10+.


## Supported tags and respective ```Dockerfile``` links

All installs include Mitogen mainly due to the performance improvements that Mitogen awards you. You can read more about it inside the [Mitogen for Ansible documentation](https://mitogen.readthedocs.io/en/stable/ansible.html).

### Immutable Images

There are a number of immutable images that are also being collected. To find a specific version of Ansible, look within the [Docker Hub Tags](https://hub.docker.com/r/willhallonline/ansible/tags). Each of the containers follow a similar pattern: **Ansible-version**-**Base OS version**.

### Ansible Core (2.12, 2.13, 2.14, 2.15, 2.16)

This includes `ansible-core` + `ansible`.

| Base Image (↓) \ Ansible Version (→) | Dockerfile                                                                                                              | 2.12                 | 2.13                 | 2.14                 | 2.15                 | 2.16 |
|--------------------------------------|-------------------------------------------------------------------------------------------------------------------------|----------------------|----------------------|----------------------|----------------------|----------------------|
| Latest                               | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine317/Dockerfile)            |                      | `latest`*            |                      |                      |                      |
| Alpine                               | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine317/Dockerfile)            |                      | `alpine`*            |                      |                      |                      |
| Ubuntu                               | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/ubuntu2204/Dockerfile)           |                      | `ubuntu`             |                      |                      |                      |
| Alpine 3.14                          | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine314/Dockerfile)            | `2.12-alpine-3.14`   | `2.13-alpine-3.14`   | `2.14-alpine-3.14`   | `2.15-alpine-3.14`   |  |
| Alpine 3.15                          | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine315/Dockerfile)            | `2.12-alpine-3.15`   | `2.13-alpine-3.15`   | `2.14-alpine-3.15`   | `2.15-alpine-3.15`   |  |
| Alpine 3.16                          | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine316/Dockerfile)            | `2.12-alpine-3.16`   | `2.13-alpine-3.16`   | `2.14-alpine-3.16`   | `2.15-alpine-3.16`   | `2.16-alpine-3.16` |
| Alpine 3.17                          | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine317/Dockerfile)            | `2.12-alpine-3.17`   | `2.13-alpine-3.17`   | `2.14-alpine-3.17`   | `2.15-alpine-3.17`   | `2.16-alpine-3.17` |
| Alpine 3.18                          | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine318/Dockerfile)            | `2.12-alpine-3.18`   | `2.13-alpine-3.18`   | `2.14-alpine-3.18`   | `2.15-alpine-3.18`   | `2.16-alpine-3.18` |
| Bullseye (Debian 11)                 | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/debian-bullseye/Dockerfile)      | `2.12-bullseye`      | `2.13-bullseye`      | `2.14-bullseye`      | `2.15-bullseye`      |  |
| Bullseye Slim (Debian 11)            | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/debian-bullseye-slim/Dockerfile) | `2.12-bullseye-slim` | `2.13-bullseye-slim` | `2.14-bullseye-slim` | `2.15-bullseye-slim` |  |
| Rocky Linux 9                        | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/rocky9/Dockerfile)               | `2.12-rockylinux-9`  | `2.13-rockylinux-9`  | `2.14-rockylinux-9`  | `2.15-rockylinux-9`  |  |
| Ubuntu 20.04                         | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/ubuntu2004/Dockerfile)           | `2.12-ubuntu-20.04`  | `2.13-ubuntu-20.04`  |                      |                      |                      |
| Ubuntu 22.04                         | [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/ubuntu2204/Dockerfile)           | `2.12-ubuntu-22.04`  | `2.13-ubuntu-22.04`  | `2.14-ubuntu-22.04`  | `2.15-ubuntu-22.04`  | `2.16-ubuntu-22.04` |

### ARM Releases 

There is some support for Arm architecture.

- `linux/arm64` (Macbook and AWS Graviton) to `latest` and `alpine` image tags.
- `linux/arm/v7` and `linux/arm/v6` to `arm` image tag (Raspberry Pi).

### Older releases

- Ansible 2.11 includes `ansible-core` + `ansible`. This also requires Python 3.
- Ansible 2.10 includes `ansible-base`.
- Ansible 2.9 includes `ansible`.

| Base Image (↓) \ Ansible Version (→) |  2.11                                                                                                                                        |  2.10                                                                                                                                        |  2.9                                                                                                                                   | 
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| Alpine 3.14                          | `2.11-alpine-3.14` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine314/Dockerfile)              | `2.10-alpine-3.14` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/alpine314/Dockerfile)              | `2.9-alpine-3.14` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/alpine314/Dockerfile)              |
| Alpine 3.15                          | `2.11-alpine-3.15` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine315/Dockerfile)              | `2.10-alpine-3.15` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/alpine315/Dockerfile)              | `2.9-alpine-3.15` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/alpine315/Dockerfile)              |
| Alpine 3.16                          | `2.11-alpine-3.16` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine316/Dockerfile)              | `2.10-alpine-3.16` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/alpine316/Dockerfile)              | `2.9-alpine-3.16` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/alpine316/Dockerfile)              |
| Alpine 3.17                          | `2.11-alpine-3.17` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/alpine317/Dockerfile)              | `2.10-alpine-3.17` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/alpine317/Dockerfile)              | `2.9-alpine-3.17` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/alpine317/Dockerfile)              |
| Bullseye (Debian 11)                 | `2.11-bullseye` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/debian-bullseye/Dockerfile)           | `2.10-bullseye` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/debian-bullseye/Dockerfile)           | `2.9-bullseye` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/debian-bullseye/Dockerfile)           |
| Bullseye Slim (Debian 11)            | `2.11-bullseye-slim` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/debian-bullseye-slim/Dockerfile) | `2.10-bullseye-slim` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/debian-bullseye-slim/Dockerfile) | `2.9-bullseye-slim` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/debian-bullseye-slim/Dockerfile) |
| Buster (Debian 10)                   | `2.11-buster` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/debian-buster/Dockerfile)               | `2.10-buster` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/debian-buster/Dockerfile)               | `2.9-buster` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/debian-buster/Dockerfile)               |
| Buster Slim (Debian 10)              | `2.11-buster-slim` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/debian-buster-slim/Dockerfile)     | `2.10-buster-slim` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/debian-buster-slim/Dockerfile)     | `2.9-buster-slim` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/debian-buster-slim/Dockerfile)     |
| Centos 7                             | `2.11-centos-7` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/centos7/Dockerfile)                   | `2.10-centos-7` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/centos7/Dockerfile)                   | `2.9-centos-7` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/centos7/Dockerfile)                   |
| Rocky Linux 8                        | `2.11-rockylinux-8` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/rocky8/Dockerfile)                | `2.10-rockylinux-8` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/rocky8/Dockerfile)                | `2.9-rockylinux-8` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/rocky8/Dockerfile)                |
| Rocky Linux 9                        | `2.11-rockylinux-9` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/rocky9/Dockerfile)                | `2.10-rockylinux-9` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/rocky9/Dockerfile)                | `2.9-rockylinux-9` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/rocky9/Dockerfile)                |
| Ubuntu 18.04                         | `2.11-ubuntu-18.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/ubuntu1804/Dockerfile)            | `2.10-ubuntu-18.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/ubuntu1804/Dockerfile)            | `2.9-ubuntu-18.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/ubuntu1804/Dockerfile)            |
| Ubuntu 20.04                         | `2.11-ubuntu-20.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/ubuntu2004/Dockerfile)            | `2.10-ubuntu-20.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/ubuntu2004/Dockerfile)            | `2.9-ubuntu-20.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/ubuntu2004/Dockerfile)            |
| Ubuntu 22.04                         | `2.11-ubuntu-22.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-core/ubuntu2204/Dockerfile)            | `2.10-ubuntu-22.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible-base/ubuntu2204/Dockerfile)            | `2.9-ubuntu-22.04` [Dockerfile](https://github.com/willhallonline/docker-ansible/blob/master/ansible/ubuntu2204/Dockerfile)            |

### Using Mitogen

To leverage *Mitogen- to accelerate your playbook runs, add this to your ```ansible.cfg```:

Please investigate in your container the location of `ansible_mitogen` (it is different per container). You can do this via:

```bash
your_container="ansible:latest"
docker run --rm -it "willhallonline/${your_container}" /bin/sh -c "find / -type d | grep 'ansible_mitogen/plugins' | sort | head -n 1"
```

and then configuring your own ansible.cfg like:

```ini
[defaults]
strategy_plugins = /usr/local/lib/python3.{python-version}/site-packages/ansible_mitogen/plugins/
strategy = mitogen_linear
```

## Running

**You will likely need to mount required directories into your container to make it run (or build on top of what is here).

### Simple

```bash
$~   docker run --rm -it willhallonline/ansible:latest /bin/sh
```

### Mount local directory and ssh key

```bash
$~  docker run --rm -it -v $(pwd):/ansible -v ~/.ssh/id_rsa:/root/id_rsa willhallonline/ansible:latest /bin/sh
```

### Injecting commands

```bash
$~  docker run --rm -it -v $(pwd):/ansible -v ~/.ssh/id_rsa:/root/id_rsa willhallonline/ansible:latest ansible-playbook playbook.yml
```

### Bash Alias

You can put these inside your dotfiles (~/.bashrc or ~/.zshrc to make handy aliases).

```bash
alias docker-ansible-cli='docker run --rm -it -v $(pwd):/ansible -v ~/.ssh/id_rsa:/root/.ssh/id_rsa --workdir=/ansible willhallonline/ansible:latest /bin/sh'
alias docker-ansible-cmd='docker run --rm -it -v $(pwd):/ansible -v ~/.ssh/id_rsa:/root/.ssh/id_rsa --workdir=/ansible willhallonline/ansible:latest '
```

use with:

```bash
$~  docker-ansible-cli ansible-playbook -u playbook.yml
```

## Maintainer

- Written and maintained by [Will Hall](https://www.willhallonline.co.uk)

[hub]: https://hub.docker.com/r/willhallonline/ansible
[microbadger]: https://microbadger.com/images/willhallonline/ansible
