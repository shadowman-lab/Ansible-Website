# Website
Website Demo for Ansible for Windows and RHEL 

# Templates

indexcomplex.html.j2
>Complex Index file for Update Webpage, uses inventory_hostname

# Playbooks
rhel_apache.yml
>tasks to setup firewalld, apache, and populate web server with html 

Web Install and Verification.yml
>Does a full web install and verification based on OS and verifies the site is up (can also be used to run updates via webhook with tags)

windows_iis.yml
>tasks to install iis, and populate web server with html
