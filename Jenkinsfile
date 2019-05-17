pipeline {
    agent any
    stages {
        stage('Test') {
            steps {
                echo 'Executing mvn test'
                sh 'mvn test'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
    }
}