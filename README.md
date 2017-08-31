# Project: Linux Server Configuration
With this project I learned installing/configuring web and database servers. In this case I used Amazon Lightsail service to host one of my web application.

DNS Address: http://ec2-18-220-184-184.us-east-2.compute.amazonaws.com
IP Address: *18.220.184.184*
SSH port: *2200*

## Summary of software I installed and configuration changes made.
- Update package index and upgrade system packages installed with `sudo apt-get update/upgrade`  command-line tools.
- Changed the SSH port from 22 default to 2200. Made sure to configure the Lightsail firewall to allow it.
- Configured the Uncomplicated Firewall (UFW) to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
- Created a new user account named grader with sudo permission. Created an SSH key pair for grader.
- Verified local timezone is set to UTC
- Installed and configure Apache to serve a Python mod_wsgi application.
- Installed and configure PostgreSQL. Created postgres catalog role and database along with a new linux user named catalog.
- Installed git and python-pip. Then installed virtualenv and psycopg2 through pip.
- Clone and installed https://github.com/jrbaez01/project-item-catalog project into /var/www/catalog and created new virtualenv.
- Created catalog.wsgi script to server catalog application using virtualenv.
- Created catalog.conf apache virtualhost into /etc/apache2/sites-available and enable using `sudo a2ensite catalog`

## List of any third-party resources you made use of to complete this project.
- https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-16-04
- http://flask.pocoo.org/docs/0.12/deploying/mod_wsgi/
- http://modwsgi.readthedocs.io/en/develop/configuration-directives/WSGIDaemonProcess.html





