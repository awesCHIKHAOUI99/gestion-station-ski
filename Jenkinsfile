pipeline {
    agent any
    environment {
registryCredentials = "nexus"
registry = "10.0.2.15:8083"
}
   
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
                  sh 'mvn test'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'mvn clean package'
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
                    docker.withRegistry("http://"+registry,
                     registryCredentials ) {
                     sh "docker push ${registry}/springBootapp:0.0"
               
                }
            }
        }
        
    }
}


