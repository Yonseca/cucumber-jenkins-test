pipeline {
    agent {
        docker {
            image 'maven:3-alpine'
            args '-v /root/.m2:/root/.m2'
        }
    }
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