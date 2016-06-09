Manati Teampass Server
======================

Since we're so lazy at Manati; we need to have our teampass server fully scripted in order to rebuild from scratch it if necessary.

## Install required roles.
`sudo ansible-galaxy install -r provisioning/requirements.yml --force`

## Prerequisites

- Copy custom.config.yml to config.yml and replace necessary values
- Your system should have python-netaddr installed (`sudo apt-get install python-netaddr`)

## Start the VM
`vagrant up`

## Start the DigitalOcean server
`vagrant up --provider=digital_ocean`

## Post Install

- Configure dns (openvpn_host should match a real dns name)
- Change admin user password to a real password
