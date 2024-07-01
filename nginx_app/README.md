# Nginx Container - Html Templates


## Prerequisites
- Docker
- Docker CLI
- Terminal
- Artifactory Access


## Assumptions
- Git
- docker cli


## Instructions

Basic container deployment for html response on multiple browser rendered endpoints. Also has
basic api endpoints for testing and hello world type examples.

/index
/second
/api
/keepalive

To run local server:
- uvicorn main:app --host 0.0.0.0 --port 8000 --reload

To deploy on AKS:
- kubectl create secret docker-registry deploy-token --docker-server=carmax-docker-local.jfrog.io 
--docker-username=<your-name> --docker-password=<your-pword> --docker-email=<your-email>

```<your-name>``` is your employee ID

```<your-pword>``` is a token from jfrog using "set me up" in the top right after logging in. Its the same as this TP 
but just use the token you generate here.

```<your-email>``` is your carmax email in the form of firstname_lastname@carmax.com

### Points of Contact
- Author: KPaaS Dev Team
