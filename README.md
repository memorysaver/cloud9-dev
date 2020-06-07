# cloud9-dev

Ansible playbook for Cloud9 development environment

Sets up a new environment within a AWS Cloud9 EC2 instance running Amazon Linux
AMI.

## Setup

```bash

# Clone repository
mkdir -p ~/environment/github/
cd ~/environment/github/
git clone https://github.com/memorysaver/cloud9-dev.git

# Install Ansible
cd ~/environment/github/cloud9-dev
/bin/bash ./setup.sh

# Copy Ansible Secrets Template to ~/.ansible_secrets.yml
# Configure with keys as needed
cp -n ansible_secrets_example.yml ~/.ansible_secrets.yml

# Install Ansible Galaxy dependencies
ansible-galaxy install -r requirements.yml

# Run Ansible playbook
ansible-playbook local.yml

```
