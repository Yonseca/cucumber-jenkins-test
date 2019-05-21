pipeline {
    agent any
    tools {
        maven 'Maven 3.3.9'
        jdk 'jdk8'
    }
    
    stages{
        stage('Test') {
            steps {
                echo 'Executing mvn test'
                powershell 'mvn test'
            }
        }
    }
    post { 
        always { 
            junit 'target/surefire-reports/*.xml'
        }
    }
}