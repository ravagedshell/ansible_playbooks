# My Ansible Playbooks
Here is my public repo of Ansible playbooks. You're free to use and modify them as you see fit.

I'm working on writing some more playbooks, but these have sufficed for my homelab needs to date. There are other items I'm working on in the future that will significantly expand my use of Ansible and hence there will be some more playbooks that get written. I'll probably change the directory structure when that time comes.

# linux-playbooks/
| File                          | Description                                                                                       |
|-------------------------------|---------------------------------------------------------------------------------------------------|
| disable-root-user.yml         | ensures the root user login is disabled (password locked and shell set to /usr/bin/nologin)       |
| dnf-update-standard.yml       | Updates all packaged on system to latest version.                                                 |
| fix-usb-freezing.yml          | Fixes the annoying issue where copying large files from USB causes system lockup.                 |
| sshd_config.yml               | Sets my standard SSHD config                                                                      |
| yum-standard-repos.yml        | Sets my standard repos to be enabled for yum/dnf                                                  |
| add-ssh-key.yml               | Adds my SSH public key to the ~/.ssh/authorized_keys file                                         |
| apt-add-defaults.yml          | Installs common utils I basically always use on a Linux box                                       |
| apt-get-upgrade.yml           | Performs standard apt-get upgrade, removes orphaned packages                                      |
| install-cisco-amp.yml         | Installs Cisco Secure Endpoint                                                                    |
| cron-auto-update.yml          | Adds a script for automatic updates to /opt/scripts and enables it to run daily at 00:00          |
 