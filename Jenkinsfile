pipeline {
    agent any
   
    stages {
        stage('Compile') { // Corrected the stage name
            steps {
                checkout scm
            }
        }
        stage('Test/Junit') {
            steps {
                script {
                   echo 'hello from test'
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
    }
}


