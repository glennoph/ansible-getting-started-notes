# ansible-getting-started-notes
notes for getting started with ansible
See https://www.udemy.com/ansible-quick-start 

## Environment setup
Vagrant was used to provision the servers
* control: running centos7 used to execute ansible scripts
* centos client running centos7
* ubuntu client running ubuntu

See Vagrantfile for details.

### Install ansible on control

access the control system with:
`vagrant ssh control`

install packages needed for ansible on centos

```bash
sudo yum install epel-release
sudo yum update
sudo yum install git python python-devel python-pip openssl ansible

```

* check that ansible is installed
```bash
ansible --version
ansible 2.4.2.0
```
* setup post install
** edit /etc/ansible/ansible.cfg
uncomment following lines:
```
inventory      = /etc/ansible/hosts
sudo_user      = root
```
