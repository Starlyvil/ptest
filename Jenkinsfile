pipeline {
    agent any
    environment {
        AA = credentials("test-credential")
    }
    stages {
        stage('Build') {
            steps {
              // withCredentials(bindings: [usernamePassword(credentialsId: 'test-credential', usernameVariable: 'UN', passwordVariable: 'PW')]){
                  // echo "my user name is ${UN} and my password is ${PW}"
              // }
                sh "echo Building code..... ${AA}"
                //sh "whoami"
               // sh "echo 'sampling' > /home/jenkins_home/abccsa123.txt"
            }
        }
        stage('Test') {
            steps (){
                sh "echo 'Testing code.....'"
            }
        }
    }
}
