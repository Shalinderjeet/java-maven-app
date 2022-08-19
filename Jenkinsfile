#!/usr/bin/env groovy

@Library('jenkins-shared-library')
def gv


pipeline {
    agent any
    tools {
        maven 'Maven'
    }    
    stages {
        stage("init") {
            steps {
                script {
                    gv = load "script.groovy"
                }
            }
        }
        stage("build jar") {
            steps {
                script {
                    echo "building jar demo90j"
                   buildJar()
                }
            }
        }
        stage("build image") {
            steps {
                script {
                    echo "building image"
                    buildImage 'shalinder/demo:jma-4.0'
                 
                }
            }
        }
        stage("deploy") {
            steps {
                script {
                    echo "deploying"
                    gv.deployApp()
                }
            }
        }
    }   
}
