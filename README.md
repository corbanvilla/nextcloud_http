# nextcloud_http
Local HTTP Nextcloud server w/ Docker

### What is it?
This is a docker-compose file and nginx conf for running nextcloud at home. It's NOT using https and assumes that if you're connecting you're either on a secure local network or using an encrypted VPN. Use at your own risk. 

### How do I use it?
It's super simple. Make sure your firewall rules allow incoming traffic on port 80, and start the containers like so:

Clone the repo:
`git clone https://github.com/corbanvilla/nextcloud_http.git`

Make sure you have docker and docker-compose installed, if not follow [the docs here](https://docs.docker.com/install/)

Change the mysql user and password:
`vim docker-compose.yml`

And start the containers:
`docker-compose up -d`

You can follow the logs to check if they started alright:
`docker-compose logs -f`

Connect to your docker host and go through the setup. The database host is: `nextcloud_db` because docker has an internal DNS resolver for networks. 
