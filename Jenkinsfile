pipeline {
    agent any
    stages {
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