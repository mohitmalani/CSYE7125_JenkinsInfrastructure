# Infrastructure as Code w/Ansible - Ansible Playbooks for AWS Infrastructure & Jenkins Setup

### Setup networking components such as VPC, subnets, route table, internet gateway, security groups and launch EC2 instance using following command:

```sh
ansible-playbook -v networking/networking-setup-playbook.yml --extra-vars "@networking-setup-var.yml"
```
### Get an SSL certificate from Let's Encrypt using certbot

```sh
ansible-playbook -v networking/jenkins-setup.yml -i hostfile --key-file <key_with_which_ec2_is_launched>.pem --extra-vars "@jenkins-setup-var.yml"
```
### Teardown Network components and EC2 instance using following command:
```sh
ansible-playbook -v networking/networking-teardown-playbook.yml"
```
