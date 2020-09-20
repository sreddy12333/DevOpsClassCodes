pipeline {
    agent any  
    stages {
        stage('Build') {
            steps {
                sh 'mvn clean'
            }
        }
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        }
        stage('compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('package') {
            steps {
                sh 'mvn package'
            }
        }
        stage("Build image") {
            steps {
             sh 'docker build -f ./var/lib/jenkins/workspace/k8s-build-pipeline/var/Dockerfile1 -t addressbook:latest .'
            }
        }
      
        
     
}
}
