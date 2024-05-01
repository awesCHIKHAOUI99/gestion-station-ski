pipeline {
    agent any
    environment {
        // Define environment variables if needed
        MAVEN_HOME = tool 'Maven'
    }
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {
            steps {
                sh "${env.MAVEN_HOME}/bin/mvn clean package"
            }
        }
        stage('Test') {
            steps {
                sh "${env.MAVEN_HOME}/bin/mvn test"
            }
        }
    }
}
