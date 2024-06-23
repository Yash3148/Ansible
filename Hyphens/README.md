Ansible Command Options

--ask-become-pass
Description: Ask for the privilege escalation password.
Usage: ansible all -m ping --ask-become-pass

--ask-pass
Description: Ask for the SSH password.
Usage: ansible all -m ping --ask-pass

--become
Description: Run operations with become (default: no).
Usage: ansible all -m ping --become

--become-method
Description: Privilege escalation method to use (default: sudo).
Usage: ansible all -m ping --become-method=sudo

--become-user
Description: Run operations as this user (default: root).
Usage: ansible all -m ping --become-user=root

--check
Description: Don't make any changes; instead, try to predict some of the changes that may occur.
Usage: ansible all -m ping --check

--diff
Description: When changing (small) files and templates, show the differences in those files; works great with --check.
Usage: ansible all -m ping --diff

--inventory or -i
Description: Specify inventory host path or comma-separated host list.
Usage: ansible all -m ping -i inventory_file

--limit or -l
Description: Further limit selected hosts to an additional pattern.
Usage: ansible all -m ping -l webservers

--module-name or -m
Description: Module name to execute (default: command).
Usage: ansible all -m ping

--private-key or --key-file
Description: Use this file to authenticate the connection.
Usage: ansible all -m ping --private-key=/path/to/keyfile

--user or -u
Description: Connect as this user.
Usage: ansible all -m ping -u ansible_user

===============================================================================================================================================

ansible-playbook Command Options

--ask-become-pass
Description: Ask for privilege escalation password.
Usage: ansible-playbook site.yml --ask-become-pass

--ask-pass
Description: Ask for SSH password.
Usage: ansible-playbook site.yml --ask-pass

--become
Description: Run operations with become (default: no).
Usage: ansible-playbook site.yml --become

--become-method
Description: Privilege escalation method to use (default: sudo).
Usage: ansible-playbook site.yml --become-method=sudo

--become-user
Description: Run operations as this user (default: root).
Usage: ansible-playbook site.yml --become-user=root

--check
Description: Don't make any changes; instead, try to predict some of the changes that may occur.
Usage: ansible-playbook site.yml --check

--diff
Description: When changing (small) files and templates, show the differences in those files; works great with --check.
Usage: ansible-playbook site.yml --diff

--inventory or -i
Description: Specify inventory host path or comma-separated host list.
Usage: ansible-playbook site.yml -i inventory_file

--limit or -l
Description: Further limit selected hosts to an additional pattern.
Usage: ansible-playbook site.yml -l webservers

--private-key or --key-file
Description: Use this file to authenticate the connection.
Usage: ansible-playbook site.yml --private-key=/path/to/keyfile

--tags
Description: Only run plays and tasks tagged with these values.
Usage: ansible-playbook site.yml --tags="configuration,setup"

--skip-tags
Description: Only run plays and tasks whose tags do not match these values.
Usage: ansible-playbook site.yml --skip-tags="configuration,setup"

--extra-vars or -e
Description: Set additional variables as key=value or YAML/JSON.
Usage: ansible-playbook site.yml -e "user=admin"

--start-at-task
Description: Start the playbook at the task matching this name.
Usage: ansible-playbook site.yml --start-at-task="Install packages"

--flush-cache
Description: Clear the fact cache.
Usage: ansible-playbook site.yml --flush-cache

===============================================================================================================================================

ansible-galaxy Command Options

--roles-path
Description: The path to the directory containing roles.
Usage: ansible-galaxy install username.role_name --roles-path=/path/to/roles

--force
Description: Force overwriting an existing role or collection.
Usage: ansible-galaxy install username.role_name --force

--no-deps
Description: Don't download roles listed as dependencies.
Usage: ansible-galaxy install username.role_name --no-deps

--offline
Description: Run the install command without accessing the network.
Usage: ansible-galaxy install username.role_name --offline

===============================================================================================================================================

ansible-doc Command Options

--list
Description: List available modules.
Usage: ansible-doc --list

--module-path
Description: Specify the module library path.
Usage: ansible-doc --module-path=/path/to/modules

--snippet
Description: Show playbook snippet for specified module(s).
Usage: ansible-doc -s module_name

--metadata-dump
Description: Dump the metadata for the specified plugin(s).
Usage: ansible-doc --metadata-dump=module_name

===============================================================================================================================================

ansible-vault Command Options

--ask-vault-pass
Description: Ask for the vault password.
Usage: ansible-vault create secrets.yml --ask-vault-pass

--vault-id
Description: Specify the vault identity to use.
Usage: ansible-vault encrypt secrets.yml --vault-id=my_vault_id

--new-vault-id
Description: Specify the new vault identity to use for rekeying.
Usage: ansible-vault rekey secrets.yml --new-vault-id=new_vault_id

--vault-password-file
Description: Specify the file to read the vault password from.
Usage: ansible-vault create secrets.yml --vault-password-file=/path/to/password_file

===============================================================================================================================================

ansible-config Command Options

--list
Description: List all configuration options.
Usage: ansible-config list

--dump
Description: Dump configuration in JSON format.
Usage: ansible-config dump

--config
Description: Specify an alternative config file.
Usage: ansible-config dump --config=/path/to/ansible.cfg
ansible-inventory Command Options

--list
Description: List inventory as JSON.
Usage: ansible-inventory --list -i inventory_file

--host
Description: Display information about a specific host.
Usage: ansible-inventory --host hostname -i inventory_file

--graph
Description: Create a graph of the inventory.
Usage: ansible-inventory --graph -i inventory_file

--yaml
Description: Display inventory as YAML.
Usage: ansible-inventory --yaml -i inventory_file

===============================================================================================================================================

ansible-pull Command Options

--accept-host-key
Description: Accept SSH host key.
Usage: ansible-pull -U https://github.com/repo.git --accept-host-key

--checkout
Description: Checkout a specific branch/tag/commit.
Usage: ansible-pull -U https://github.com/repo.git --checkout my_branch

--directory
Description: Directory to clone into.
Usage: ansible-pull -U https://github.com/repo.git --directory=/path/to/dir

--full
Description: Do a full clone without --depth=1.
Usage: ansible-pull -U https://github.com/repo.git --full

===============================================================================================================================================

ansible-test Command Options

--docker
Description: Use Docker containers for tests.
Usage: ansible-test integration --docker

--python
Description: Specify Python interpreter to use.
Usage: ansible-test integration --python=python3.8

--requirements
Description: Install test requirements.
Usage: ansible-test sanity --requirements

===============================================================================================================================================

General Options

--version
Description: Show the version number and exit.
Usage: ansible --version

--help
Description: Show help message and exit.
Usage: ansible-playbook --help
===============================================================================================================================================
