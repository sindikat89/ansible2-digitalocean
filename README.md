# Ansible2 DigitalOcean APIv.2
Server provisioning playbook for DigitalOcean droplets

##Prerequisites:
1. Linux native environment with Ansible2 dependencies installed
2. <a href="https://m.do.co/c/0a8cc915e6ef">DigitalOcean</a> account
3. Login to <a href="https://m.do.co/c/0a8cc915e6ef">DigitalOcean</a> account and navigate to API -> TOKENS
4. Generate New Token named digital_ocean and copy it to clipboard
> Navigate to Linux environment and open CLI

5. Run the following commands
  * **export DO_API_TOKEN=<--PASTE COPIED TOKEN HERE-->**
  * **cd ~/.ssh/**
  * **ssh-keygen -t rsa -f LOCAL (on prompt HIT ENTER)**
  * **ssh-keygen -t rsa -f REMOTE (on prompt HIT ENTER)**
  * **sudo chown root:root REMOTE**
  * **sudo chown root:root REMOTE.pub**
  * **sudo apt-get install xclip**
  * **cat ./LOCAL.pub|xclip -i -selection clipboard**
6. Open <a href="https://m.do.co/c/0a8cc915e6ef">DigitalOcean</a> account in browser and navigate to SETTINGS -> SECURITY
7. ADD New SSH Key name: LOCAL and paste SSH key content
> Navigate to Linux environment and open CLI

8. Run command
  * **cat ./REMOTE.pub|xclip -i -selection clipboard**
9. Open <a href="https://m.do.co/c/0a8cc915e6ef">DigitalOcean</a> account in browser and navigate to SETTINGS -> SECURITY
10. ADD New SSH Key name: REMOTE and paste SSH key content
11. Final step: Edit the **ansible_user** variable in the **hosts** file to your Linux user

Finally in CLI navigate to the cloned projects main directory and run **ansible-playbook provision_servers.yml**

Also you can run the "ansible-playbook destroy_droplets.yml" playbook to destroy the droplets.

Cheers!

PERSONAL NOTE
---
I would appreciate if you use the refferal link if new to <a href="https://m.do.co/c/0a8cc915e6ef">DigitalOcean</a>!
