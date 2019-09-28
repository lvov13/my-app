pipeline {
    agent any 
    tools { 
        maven 'localMAVEN'
    }
    stages {
        stage('clone repository and clean') { 
            steps {
            sh "mvn clean"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package"  
            }
        }
    }
}