ANSIBLE - AUTHENTICATION

Create ansible service account

This document covers the following items:
  1 Create an account called svc_ansible
  2 Grent root privileges


1 - Create an account called svc_ansible
    run the commands below:
      sudo useradd svc_ansible
      (Note the password is not required, due authentication is predicted to be done via keys)
 
2 - Grant root privileges
    run the command below:
      sudo visudo
      add the line: svc_ansible ALL=(ALL) NOPASSWD:ALL
