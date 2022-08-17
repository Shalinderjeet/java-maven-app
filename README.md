Title:- Create a CI Pipeline with Jenkins file (Freestyle, Pipeline ,Multibranch Pipeline)

Description:- CI Pipeline for a Java Maven application to build and push to the repository

Install Build Tools (Maven) in Jenkins

Create Jenkins credentials for a git repository

Give Docker path in shell script on Jenkins server.


Create different Jenkins job types(Freestyle,Pipeline,Multibranchpipeline)for the Java Maven project with Jenkins file to : Connect to the application's git repository Build Jar Build Docker Image Push to private DockerHub Repository

a) Freestyle Project/jobs:- Configure github connection, run maven command to package the java project that will create a jar file and then run docker command to build a dockerfile. Check Freestyle.* screenshots.

b) Pipeline Job:-
