pipeline {
    agent any
    tools {
          maven 'maven-3.6.3'
    }
    stages {
        stage('Build') {
            steps {
               bat 'mvn clean install'
            }
        }
        stage('Deploy') {
            steps {
               bat 'mvn package'
            }
        } 
    }
}
