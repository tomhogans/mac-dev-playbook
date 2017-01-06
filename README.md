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
