Ansible Playbook to install Gitea on an Ubuntu 18.04+ server

The instructions for installing gitea can be found here:

https://docs.gitea.io/en-us/install-from-binary/

Using those commands, I built a quick Ansible playbook to install the package on a fresh install of Ubuntu 18.04+ server

Assumptions:
The user you're installing this as has their id_rsa.pub key copied to the host you're installing gitea on
the /etc/sudoers file allows the sudo users to not have to type in a password.

This playbook doesn't restore the backup yet, but it will...

That is all.



RESTORE NOTES:

Follow these steps to restoring:

0. Make sure that gitea is installed and configured
1. Copy the backup dump to the git user's home directory
2. unzip gitea-dump-1482906742.zip
3. unzip gitea-repo.zip
4. cp app.ini /etc/gitea/app.ini
5. cp gitea.db /var/lib/gitea/data/
6. sudo systemctl restart gitea
