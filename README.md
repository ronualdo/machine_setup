# Machine Setup

Ansible playbook used to setup my personal environment.

## Prequisites
- Ansible
- Git

## Usage

This playbook makes usage of a var file that provides needed
information. To use it, make sure to create this file in home
folder

```
touche ~/.setup_vars
```

And fill it with the following information:

```
user: <<user to be setted up>>
workspace_folder: <<folder where repositories will be checked out>>
```

After having that in place, just run the following command to
run playbook

```
ansible-pull -K -U https://github.com/ronualdo/machine_setup.git
```

The command will ask for the user password. The user should have
permission to run `sudo` in the system. After providing that
playbook should run and provision the workstation.
