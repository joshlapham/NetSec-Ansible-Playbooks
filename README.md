## NetSec - Ansible Playbooks

By Josh Lapham [josh@joshlapham.com]

License: [Beerware](https://en.wikipedia.org/wiki/Beerware)

### What This Is

[Ansible playbooks](http://docs.ansible.com/ansible/playbooks.html) for provisioning a new [Debian](https://www.debian.org/) box for security and penetration testing.

Right now this just installs [Damn Vulnerable Web Application](https://github.com/RandomStorm/DVWA).

### How to Use

1. [Install Ansible](http://docs.ansible.com/ansible/intro_installation.html) on your local machine
2. Generate an SSH public key on your local machine: `ssh-keygen`
3. Copy SSH public key to authorized keys file on remote server instance: `~/.ssh/authorized_keys`
4. Update remote server instance address for Ansible to connect to in `cfg/staging` file
5. Update remote server instance user for Ansible to connect to in `cfg/staging` file

### Install

Once setup, run the main playbook: `ansible-playbook -i cfg/staging -s site.yml`
