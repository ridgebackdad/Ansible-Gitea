Ansible Playbook to install Gitea on an Ubuntu 18.04+ server

The instructions for installing gitea can be found here:

https://docs.gitea.io/en-us/install-from-binary/

Using those commands, I built a quick Ansible playbook to install the package on a fresh install of Ubuntu 18.04+ server

Assumptions:
The user you're installing this as has their id_rsa.pub key copied to the host you're installing gitea on
the /etc/sudoers file allows the sudo users to not have to type in a password.

This playbook doesn't restore the backup yet, but it will...

That is all.
