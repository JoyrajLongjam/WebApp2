pipeline {
    agent any
    tools {
        maven 'maven-3.6.3'
    }
    environment {
        BUILD_PATH = "target"
        WAR_NAME = "MyWebApp.war"
        TOMCAT_PATH = "C:/Program Files/Apache Software Foundation/Tomcat 9.0_Tomcat93/webapps"
    }
    stages {
        stage('Build') {
            steps {
                bat "mvn clean install"
            }
        }
        stage('Deploy to Tomcat') {
            steps {
                bat "copy ${BUILD_PATH}\\${WAR_NAME} \"${TOMCAT_PATH}\\${WAR_NAME}\""
            }
        }
    }
}


