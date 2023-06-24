pipeline {
    agent any
    environment {
        AA = credentials('test-credential')
    }
    stages {
        stage('my-stage') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'test-credential', usernameVariable: 'UN', passwordVariable: 'PW')]) {
                    echo "My username is ${UN} and my password is ${PW}"
                }
            }
        }
        stage('Test') {
            steps {
                sh "echo 'Testing code.....'"
            }
        }
    }
}
