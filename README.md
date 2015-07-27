# docker-flask-example
A generic python/Flask app with a Docker file


# How to Use this Repository
* First, fork the repo
* Create a dockerhub account at dockerhub.com
* Click the Add repository button -> Choose automated build
* Select github as the source
* Select this newly forked repository
* Fill out the name, whether the repo is public or private, etc.
* Now, evertime you push to your fork of this repository, a new Docker image will automatically build for you.

# Running your Docker Image in Production
* Create an AWS account
* Create an AWS instance in a public facing subnet, Amazon linux image
* SSH into machine ssh -i aws.pem ec2-user@[public-dns]
* yum update -y
* yum install -y docker
* service docker start
* usermod -a -G docker ec2-user
* yum install -y git
* docker login -e '[email]' -p '[password]' -u '[username]'
* docker pull [username]/[repo-name]
* docker run -p [external-facing-port]:[internal-facing-port] "-v /home/ec2-user/keys:/opt/code/keys -e [variable_name]=[variable_value] -d --name [container-name] [username]/[repo-name]

Getting Started with Docker
===========================
https://docs.docker.com/mac/started/
