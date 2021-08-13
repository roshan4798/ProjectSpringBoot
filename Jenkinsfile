pipeline {
    agent any

 

    stages {
        stage('Checking Version') {
            steps {
                sh 'javac -version'
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
        
        stage('Deploying') {
            steps {
                echo 'getting deployed'
            }
        }
    }
}
