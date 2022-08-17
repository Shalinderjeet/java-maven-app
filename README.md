Title:- Create a CI Pipeline with Jenkins file (Freestyle, Pipeline ,Multibranch Pipeline)

Description:- CI Pipeline for a Java Maven application to build and push to the repository


Create different Jenkins job types(Freestyle,Pipeline,Multibranchpipeline)for the Java Maven project with Jenkins file to : 

Connect to the application's git repository 
Build Jar 
Build Docker Image 
Push to private DockerHub Repository

a) Freestyle Project/jobs:- Configure github connection, run maven command to package the java project that will create a jar file and then run docker command to build a dockerfile. Check Freestyle.* screenshots.

Detailed Steps:-
Install Jenkins directly on Mac/Windows Operating System, access it through browser on port 8080
Install Build Tools (Maven) in Jenkins through jenkins Plugin
Connect to git repositrory in Jenkins job configuration
Give Docker binary path (instaled on operating system) in shell script on Jenkins server and run docker commands to build the dockerfile.

b) Pipeline Job:-Run Jenkins as a container on Digital Ocean Droplet (Attach firewall rules, open port 8080)

