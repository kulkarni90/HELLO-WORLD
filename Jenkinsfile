#!/usr/bin/env groovy
pipeline {
    agent any
    tools {
            ant 'Ant 1.9.1' 
            jdk 'JAVA 1.8'
    }
    stages {
        stage('Build') {
            steps {
                echo 'maven clean'
                //ABC indicates the folder name where the pom.xml file resides
                bat ' mvn -f build.xml clean install'  
                 }
          }
            post {
                success {
                    echo 'Now Archiving'
                }
            }
        }
    }

