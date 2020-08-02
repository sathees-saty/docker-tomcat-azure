Create resource group: satyconrg
-------
create container registry: as below (you can give unique name as per your requirement)
registry name: satycon.azurecr.io
satycon
satycon.azurecr.io
satycon
=ar4Cmkgb5jPlO7acqHvKfTxUcVw+vEI
RtHhuwhiy2Q99RVRw+y5J0RZkMqbFQoT
--------
source code in bellow directory. you can download from github 
cd D:\nodejs\demoapps\docker-tomcat-azure
run >docker images
-----
run
>docker build -t satycon.azurecr.io/docker-tomcat-azure:latest .
>docker images 
------
run you can change port number
>docker run -p 8082:8080 satycon.azurecr.io/docker-tomcat-azure:latest
run in terminal browser
http://localhost:8082/
-----
log in to Azure registry from terminal:
>docker login satycon.azurecr.io
enter user name
enter password
login succesfull
>docker push satycon.azurecr.io/docker-tomcat-azure:latest
---
go and check azure container repository for the latest version
---
create web apps and select docker container
dockerdemosaty, in next step select azure container registry
created
get url and open in browser
https://satyweb.azurewebsites.net
working fine
----
enable CI and DI in web apps in container settings
and save
update war file
>docker build -t satycon.azurecr.io/docker-tomcat-azure:latest .

run bellow commnad
>docker push satycon.azurecr.io/docker-tomcat-azure:latest
refersh the URL you can see the changes
-----
if you are using free tier, delete resource group and all resouces after lab. otherwise
you will charged for the resouces
-----





# docker-tomcat-satylearning
A basic tutorial on running a web app on Tomcat using Docker - SATYLearning - Subscribe my youtube channel

# Steps
* Install [Docker](https://docs.docker.com/install/).
* Clone this repository - $git clone https://github.com/sathees-saty/docker-tomcat-satylearning.git
* cd docker-tomcat-satylearning # from your root directory
* $docker build -t satymywebapp .
* $docker run -p 8082:8080 satymywebapp
* http://localhost:8082
