# ansible2-digitalocean
Server provisioning playbook for DigitalOcean droplets

Prerequisites:
- Linux native environment with Ansible2 dependencies installed
- DigitalOcean account
- Login to DigitalOcean account and navigate to API -> TOKENS
- Generate New Token named digital_ocean and copy it to clipboard
- On native Linux environment run the following commands from CLI
  * export DO_API_TOKEN=<--PASTE COPIED TOKEN HERE-->
  * cd ~/.ssh/
  * ssh-keygen -t rsa -f LOCAL (on prompt HIT ENTER)
  * ssh-keygen -t rsa -f REMOTE (on prompt HIT ENTER)
  * sudo chown root:root REMOTE
  * sudo chown root:root REMOTE.pub
  * sudo apt-get install xclip
  * cat ./LOCAL.pub|xclip -i -selection clipboard
 - Open DigitalOcean account in browser and navigate to SETTINGS -> SECURITY
 - ADD New SSH Key named LOCAL and paste copied ssh-key
 - On native Linux environment run the following commands from CLI
  * cat ./REMOTE.pub|xclip -i -selection clipboard
 - Open DigitalOcean account in browser and navigate to SETTINGS -> SECURITY
 - ADD New SSH Key named REMOTE and paste copied ssh-key

Finally in CLI navigate to the cloned projects main directory and run 'ansible-playbook site.yml'

Cheers!

_______________________________PERSONAL NOTE_________________________________

  ******  I would appreciate if you use the refferal link if new to DigitalOcean! ******
