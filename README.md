Title:- Create a CI Pipeline with Jenkins file (Freestyle, Pipeline ,Multibranch Pipeline) using webhooks (Trigger Pipeline jobs automatically)

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

docker build -t shalinder/demo:java-maven-app-1.0 .
echo $PASSWORD | docker login -u $USERNAME --password-stdin
docker push shalinder/demo:java-maven-app-1.0

------------------------------------------------------------------------------------------------------------------------------------------------
b) Pipeline:-Run Jenkins as a container with docker installation on Jenkins on Digital Ocean Droplet (Attach firewall rules, open port 8080)

Create Jenkinsfile and groovy.script files with all the scrpts codes. Setup the pipleline by connecting to the GIT repo choosing Jenkinsfile from SCM option.
Please check the pipeline1.png for viewing the executed CI Pipeline

----------------------------------------------------------------------------------------------------------------------------------------------------------
c) Multi branch Pipeline
Create a multi branch pipeline with JenkinsfileMulti that will only run build and deploy on Main branch and not on jenkins-jobs branch as per the logic inside the Jenkins file.
Check Multibranch.*png screenshots
