# My Ansible Playbooks
Here is my public repo of Ansible playbooks. You're free to use and modify them as you see fit.

I'm working on writing some more playbooks, but these have sufficed for my homelab needs to date. There are other items I'm working on in the future that will significantly expand my use of Ansible and hence there will be some more playbooks that get written. I'll probably change the directory structure when that time comes.

# Linux Playbooks (linux-playbooks/)

| Playbook ID                   | File                                 | Description                                                                                        |
|-------------------------------|--------------------------------------|----------------------------------------------------------------------------------------------------|
| 01                            | debian-apt-get-upgrade.yml           | Performs standard apt-get upgrade, removes orphaned packages on debian based systems.              |
| 02                            | debian-cron-auto-update.yml          | Adds a script for automatic updates and enables it to run daily at 00:00 on debian based systems.  |
| 03                            | debian-install-cisco-amp.yml         | Installs Cisco Secure Endpoint on debian based systems.                                            |
| 04                            | debian-uninstall-cisco-amp.yml       | Removes Cisco Secure Endpoint from debian based systems.                                           |
| 05                            | devnet-apt-add-defaults.yml          | Installs common utils I'm using during my DevNet Studies.                                          |
| 06                            | fedora-dnf-update-standard.yml       | Updates all packaged on system to latest version on my fedora boxes.                               |
| 07                            | fedora-yum-standard-repos.yml        | Sets my standard repos to be enabled for yum/dnf on my fedora Boxes.                               |
| 08                            | linux-add-ssh-key.yml                | Adds my SSH public key to the ~/.ssh/authorized_keys file to all linux boxes.                      |
| 09                            | linux-cisco-amp-debug.yml            | Runs a debug on any linux host running CSE and exports it to selected directory.                   |
| 10                            | linux-disable-root-user.yml          | Disables the root user to ensure no-login on all linux boxes.                                      |
| 11                            | linux-fix-usb-freezing.yml           | Fixes USB freezing on large copy on all linux boxes.                                               |
| 12                            | linux-sshd_config.yml                | Sets standard SSHD config on all inux boxes (security related).                                    |


# Sample Inventory
The sample inventory is provided based on the groupings that I've defined in the playbooks, put hosts into the approriate groups and everything should run out of box.

# Running a Playbook
```bash
 ansible-playbook -i sample_inventory.yml linux-playbooks/linux-fix-usb-freezing.yml --ask-become-pass --user <your-remote-username> --ask-pass
```