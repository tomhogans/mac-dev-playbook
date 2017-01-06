# Mac Development Ansible Playbook

This repository is a fork of Jeff Geerlings excellent repository: https://github.com/geerlingguy/mac-dev-playbook

For installation:
 
    $ xcode-select --install
    $ sudo easy_install pip
    $ sudo pip install ansible
    $ git clone git@github.com:tomhogans/mac-dev-playbook.git && cd mac-dev-playbook
    $ export EMAIL="user@domain.com"
    $ export CREDENTIALS_PATH="/Volumes/USBKey/"
    $ ansible-galaxy install -r requirements.yml
    $ ansible-playbook -i inventory --ask-become-pass main.yml

The credentials file is expected to be `credentials.zip.gpg`.  Unzipped, it should have the format:

    credentials.zip
    ├── autoenv
    │   └── project1.env
    │   └── project2.env
    ├── gpg
    │   ├── myprivatekey.asc
    ├── ssh
    │   ├── config
    │   ├── my.key
    └── vpn
        ├── org
        │   └── config.ovpn
