### Project 7 - Linux Server Configuration ###

##### Connection Info #####
- IP address and SSH port: 52.36.38.198 | 2200
- Complete URL: http://ec2-52-36-38-198.us-west-2.compute.amazonaws.com/

##### Installed Software #####
  - sudo apt-get install apache2
  - sudo apt-get install libapache2-mod-wsgi
  - sudo apt-get install git
  - sudo apt-get install python-pip
  - sudo apt-get install ec2-api-tools
  - sudo apt-get install postgresql postgresql-contrib
  - sudo apt-get install python-pycopg2
  - sudo apt-get install libpq-dev
  - sudo pip install --upgrade google-api-python-client
  - pip install SQLAlchemy
  - pip install flask

##### Configuration Changes Made #####
  - Updated UFW to only allow:
    - SSH on port 2200
    - HTTP on port 80
    - NTP on port 123
  -  Created grader user
  - Created catalog database, added catalog user, gave various permissions on catalog database to catalog user
  - Changed postgres connection info to trust local connections. Remote connections to postgres remain disabled.
  - Added wsgi configuration to vend item catalog application