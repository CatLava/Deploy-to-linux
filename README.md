# Deploy-to-linux

This Readme is to outline everything maintained and included in this Ubuntu 16 Server.
-ip: 34.213.226.45
-url: 34.213.226.45.xip.io 

Server is deployed from a previous catalog project seen here. https://github.com/CatLava/Catalog
The deployment is made possible with apache2 an WSGI combination. WSGI enables appropriate routing
when navigating the webpage. The WSGI config page is directed to the main application (application.py) script
with associated error logs.

Appropraite security measures were taken with this server to lock it down. For example changing configs in the sshd_config 
file to allow port 2200 ssh and to prevent root ssh. Access to this server is only allowed with the appropriate private key
that was passed along in the Udacity assignment. The public key was uploaded to the authorized_keys folder of the grader user and given appropriate permissions. 

**For example see some steps to configure server.**
1. adduser grader : This added a user 
2. ufw allow 2200/tcp : This will allow 2200 SSH
3. ufw delete (ssh rule number): 
4. sudo nano /etc/ssh/sshd_config : this will open the editor to configure sshd rules
5. /var/www/html/Catalog : Is where error logs and application is routed and stored

There were many ancillary steps to this, but the above give a general taste of what was need. Also think packages to install
This may vary if deployment is not on an Ubuntu server.

Config: This server is configured with

http : 80
ssh : 2200
ntp : 123


**Packages included**
Python 2.7 (Please see the Catalog repo for specific python libraries)
Apache2
WSGI
sqlite

**Acknowledgements:** 
I would like to acknowledge all contributors of the Udacity Full stack to make this project possible.
Also all people who contribute to stack overflow is a huge help
Lastly, Amazon web services for their easy to use servers. 
