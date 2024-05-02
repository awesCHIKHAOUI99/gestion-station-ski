pipeline {
    agent any
   
    stages {
        stage('git checkout') { // Corrected the stage name
            steps {
                checkout scm
                
            }
        }
         stage('Compile') { // Corrected the stage name
            steps {
                
                 sh 'mvn compile'
            }
        }
        stage('Test/Junit') {
            steps {
                script {
                  sh 'mvn clean'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    echo 'hello from build'
                }
            }
        }
        stage('Sonar') {
            steps {
                script {
                    echo 'hello from sonar'
                }
            }
        }
        stage('Nexus') {
            steps {
                script {
                    echo 'hello from Nexus'
                }
            }
        }
        
    }
}


