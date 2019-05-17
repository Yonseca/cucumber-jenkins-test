pipeline {
    agent any

    stages {
        stage('Test') {
            steps {
                sh 'mvn test'
            }
        } 
    } post {
        success {
            junit 'target/surefire-reports/**/*.xml' 
        }
    }
}