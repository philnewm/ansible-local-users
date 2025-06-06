# Local-users-Role

[![Alma9-CI](https://github.com/philnewm/ansible-local-users/actions/workflows/alma9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-local-users/actions/workflows/alma9-ci-caller.yml)  [![Rocky9-CI](https://github.com/philnewm/ansible-local-users/actions/workflows/rocky9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-local-users/actions/workflows/rocky9-ci-caller.yml)  [![CentOSStream9-CI](https://github.com/philnewm/ansible-local-users/actions/workflows/centosstream9-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-local-users/actions/workflows/centosstream9-ci-caller.yml)  [![Debian12-CI](https://github.com/philnewm/ansible-local-users/actions/workflows/debian12-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-local-users/actions/workflows/debian12-ci-caller.yml)  [![Ubuntu2204-CI](https://github.com/philnewm/ansible-local-users/actions/workflows/ubuntu2204-ci-caller.yml/badge.svg)](https://github.com/philnewm/ansible-local-users/actions/workflows/ubuntu2204-ci-caller.yml)

Create/Update and delete local users based on a `.yaml` file.

This role includes a vagrant based molecule testing setup as a submodule at `molecule/`

## Structure

```code
📦 ansible-local-users
 ┣ 📂 defaults
 ┃ ┗ 📜 main.yml
 ┣ 📂 files
 ┃ ┗ 📜 default_users.yml
 ┣ 📂 meta
 ┃ ┗ 📜 main.yml
 ┣ 📂 molecule
 ┃ ┗ 📂 default
 ┃   ┗ 📜, 📜, 📜, scenario_files
 ┣ 📂 tasks
 ┃ ┣ 📜 absent.yml
 ┃ ┣ 📜 apply_users.yml
 ┃ ┣ 📜 dependencies.yml
 ┃ ┣ 📜 main.yml
 ┃ ┣ 📜 present.yml
 ┃ ┣ 📜 remove_users.yml
 ┃ ┗ 📜 tests.yml
 ┗ 🗒️ README.md
 ┗ 📓 requirements.txt

```

Describe and explain role structure.

## Requirements

Elaborate external dependencies and how to use them.

## Role Variables

* defaults/main.yml
  * first_var
  * sec_var
  * third_var
* vars/main.yml
  * first_var
  * sec_var
  * third_var

## Dependencies

List role ansible-galaxy dependencies - if any.

## Example Playbook

Add an example playbook

```yaml
---

tasks:
  - name: Include ansible-local-users present
    ansible.builtin.include_role:
      name: ansible-local-users
    vars:
      state: present

...
```

## License

Add license - if any.

## Notes

Includes special git configuration for submodule files that are most likely to get local overrides
`.git/info/attributes`

```code
molecule/default/cleanup.yml merge=ours
molecule/default/converge.yml merge=ours
molecule/default/verify.yml merge=ours
```

## Changes to role template

* Add github action that flags empty directories on release creation
