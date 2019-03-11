ANSIBLE - AUTHENTICATION

SSH Generate and copy keys

This document covers the following items:
  1 Generate a public and private keys
  2 Copy the private key to the list of known hosts

1 - Generate a public and private keys
    - sudo su svc_ansible
    - cd /home/svc_ansible
    - ssh-keygen
        - does not set any password, just complete the wizard
    - sudo cp .ssh/id_rsa /home/iac/.ssh
        - allow the user iac to use this key to authenticate on hosts
    - sudo ssh-copy-id -i ./ssh/id_rsa.pub svc_ansible@remotehost
        - Remember to create the user svc_ansible and then grant root permissions
        - You can do it following the procedure "create_ansible_account.md"
    - cp ./ssh/id_rsa /home/iac/.ssh
        - This command is required to allow iac user to use key for connections

