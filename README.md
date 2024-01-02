# Ansible role [git_tag](https://galaxy.ansible.com/ui/standalone/roles/buluma/git_tag/documentation)

Ansible role to tag github repos.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-git_tag/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-git_tag/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-git_tag.svg)](https://github.com/buluma/ansible-role-git_tag/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-git_tag.svg)](https://github.com/buluma/ansible-role-git_tag/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-git_tag.svg)](https://github.com/buluma/ansible-role-git_tag/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/git_tag)](https://galaxy.ansible.com/ui/standalone/roles/buluma/git_tag/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-git_tag/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  vars:
    git_tag: "{{env}}-{{ansible_date_time.date}}"
    skip_if_tag_matching: "{{env}}*"
    git_remote: origin

  tasks:
    - name: "Include buluma.git_tag"
      include_role:
        name: "buluma.git_tag"
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-git_tag/blob/master/defaults/main.yml):

```yaml
---
# defaults file for git_tag
git_repo_location: .
# git_remote: origin
update_git_tag: false
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-git_tag/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.git](https://galaxy.ansible.com/buluma/git)|[![Ansible Molecule](https://github.com/buluma/ansible-role-git/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-git/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-git.svg)](https://github.com/shadowwalker/ansible-role-git)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-git_tag/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[Debian](https://hub.docker.com/repository/docker/buluma/debian/general)|all|
|[Ubuntu](https://hub.docker.com/repository/docker/buluma/ubuntu/general)|all|
|[EL](https://hub.docker.com/repository/docker/buluma/enterpriselinux/general)|all|
|[Fedora](https://hub.docker.com/repository/docker/buluma/fedora/general)|all|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-git_tag/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-git_tag/blob/master/CHANGELOG.md)

## [License](#license)

[license (Apache-2.0)](https://github.com/buluma/ansible-role-git_tag/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)

