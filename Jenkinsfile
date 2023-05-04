pipeline {
    agent {
        label 'docker-slave-python'
        
    }

    stages {
        stage('Checkout') {
            steps {
                git credentialsId: 'github-cred', branch:'main', url:'https://github.com/giovannidisanto/argentea-repo-test.git'
            }
        }
        stage('Build') {
            steps {
                sh 'python3.6 hello.py'
            }
        }
        
        stage('Test') {
            steps {
                echo 'Test step'
            }
        }
        
        stage('Deploy') {
            steps {
                echo 'Deploy step'
            }
        }
    }
}
