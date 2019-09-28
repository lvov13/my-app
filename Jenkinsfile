pipeline {
    agent any 
    tools { 
        maven 'localMAVEN'
    }
    stages {
        stage('clone repository and clean') { 
            steps {
            sh "rm -rf my-app"
            sh "git clone https://github.com/lvov13/my-app.git"
            sh "mvn clean -f my-app"
            }
        }
        stage('Test') { 
            steps {
                sh "mvn test -f my-app" 
            }
        }
        stage('Deploy') { 
            steps {
                sh "mvn package -f my-app"  
            }
        }
    }
}