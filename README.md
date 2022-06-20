The playbook webserver.yml is used to install and configure apache to the webservers. 

A simple jinja2 template is deployed to /var/www/html/index.html which pulls the server's hostname from an ansible fact.

Haproxy is used as the load balancer and deploys the round robin menthod to balance the load between the two servers.
A template is also used here so the config can be easily changed in future and reapplied by running the playbook again. 

Firewalld is included in the playbook for environments where an external firewall is not presenti for security purposes. 
