pipeline {
    agent any

 

    stages {
        
        stage('Build') {
            steps {
                sh 'mvn -X clean -X package'
            }
        }
        
        stage('Deploying') {
            steps {
                deploy adapters: [tomcat8(credentialsId: '5ab4f297-992b-48df-b64f-b34f7c7fcfb2', path: '', url: 'http://35.154.186.252:8080/')], contextPath: 'DemoWebApp', war: '**/demoaws-0.0.1-SNAPSHOT.war'
            }
        }
    }
}
