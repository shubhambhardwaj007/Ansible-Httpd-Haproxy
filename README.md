# Ansible-Httpd-Haproxy
## Lets understand the Problem Statement:
1. Create an Ansible Role to configure Apache Httpd Software on Backend Web Server Remote systems.
2. Create an Ansible Role to configure Haproxy LoadBalancer Software on Frontend Server Remote systems.
3. Dynamically Update the Haproxy Loadbalancer Configuration file with Backend Apache Httpd webserver IP Addresses and restart its service.
## To replicate same setup on your Local Machine perform following steps:
- Install Ansible on local system and this local machine acts as `Master Node`.
- Clone this repository on Local Machine and edit `hosts` file to add up IP Addresses of Backend Webserver and Haproxy server.
- Edit `Ansible-Haproxy-Role/vars/main.yml` file to tell about Exposed Haproxy LoadBalancer Port Number using variable `exposed_port_number`.
- Edit `Ansible-Haproxy-Role/vars/main.yml` file to tell about  Backend Webserver Port Number using variable `webserver_port`
- Copy WebPage you like to deploy on webserver to `roles/Ansible-Httpd-Role/files/` and edit `roles/Ansible-Httpd-Role/vars/main.yml` to tell about webpage.
- Go Inside `Ansible-Httpd-Role/vars/main.yml` folder and edit `web_page_deploy` given variable to tell about New WebPage.
### Finally all things set so it's time to Deploy above complete setup and run below command:
> ansible-playbook <name_of_playbook>

## Detailed Article: [Ansible-Httpd-Haproxy Article](https://www.linkedin.com/pulse/configuring-haproxy-loadbalancer-via-ansible-shubham-bhardwaj)
