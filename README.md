# Udacity Project 6: Setup a Linux Server
### Critical information
IP Address: 35.177.216.90 port: 2200

URL: http://35.177.216.90.xip.io/

Summary of Software Installed:
- python-dev
- python-pip
- postgresql
- sqlite3 (didn't end up using)
- apache2
- apache2-utils
- libexpat1
- ssl-cert
- libapache2-mod-wsgi
- flask
- packaging
- oauth2client
- redis
- passlib
- itsdangerous
- flask-httpauth
- bleach
- requests
- flask-sqlalchemy
- sqlalchemy
- psycopg2-binary (didn't directly use as SQLAlchemy has good PSQL drivers)
- virtualenv (didn't end up using)
- and all associated dependencies

Summary of Configurations:
- Changed SSH port to 2200
- Changed Ubuntu user password to something personal
- Added user grader
- Changed 'PermitRootLogin' value to no
- Granted grader sudo permission through file /etc/sudoers.d/grader
- Changed Lightsail Firewall to accept TCP on port 2200 and close port 22
- Setup Linux Firewall rules allowing ports 2200, 80 and 123 and enabled
- Run 'sudo apt-get update && sudo apt-get upgrade'
- Installed a public key for user Grader
- Checked that PasswordAuthentication is set to no

List of Third Party Resources:
I'm not sure of anything outside of those things listed above in the sofware downloaded for the project.

### Project Rubric
This loose outline of this project is to achieve the following:
- Setup a linux server from scratch and have it serve the Item Catalog Python
project from earlier in the nanodegree.

The rubric included the following:
1) Submit the SSH private key for the 'grader' user with the project (done)
2) Block logging in as 'root' (done)
3) Give 'grader' access to run sudo commands (done)
4) Set the firewall to accept only HTTP(80), SSH(2200) and NTP(123) (completed
  on both the Lightsail firewall and the server's UFW settings)
5) Key based authentication is enforced (done)
6) Update all the system packages (done at the beginning and also prior to submission)
7) Host SSH on a non-default port (done, presently 2200 instead of 22)
8) Run a webserver on port 80 (done, it is serving my python project)
9) Configure the server's database to serve data (done, PSQL is the flavour of the month)
10) Serve the item catalog project (done)
11) Is the README written? (I certainly hope so)

### Setting up the server
This part of the project was remarkably straightforward, setting up users and their access
rights was a lot easier than navigating the process of getting the webserver to do what I
wanted to get done.
Roughly I went through the list in this order and not without problems along the way, however
thankfully it all worked out in the end and hopefully you believe the same.

### Setting up the webserver
This part was a big pain of user permissions that I expect I'll get better at
navigating the more I do it. Some of my biggest problems were:
- Installing all the project dependencies
- Attempting to make SQLite work (I ended up dropping it for PSQL)
- Navigating user permissions (www-data vs ubuntu vs root, it was joyful)
- Understanding the error logs from Apache and how to google/stack-overflow my way to success

This was a rather harrowing exercise, but I am glad that I managed to get through it all
and understand that now that I've done it once, doing it again with a new technology will
be an interesting exploration and I look forward to tackling it all again.

I now submit this project and keep my fingers crossed for problem free completion.

If there are any problems/questions/suggestions, please contact *Ben* at *benrconway84@gmail.com*
