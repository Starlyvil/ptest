pipeline {
    agent any
    stages (){
        stage('Build') {
            steps {
                sh "echo Building code....."
                sh "whoami"
               // sh "echo 'sampling' > /home/jenkins_home/abccsa123.txt"
            }
        }
        stage('Test') {
            steps {
                sh "echo 'Testing code.....'"
            }
        }
    }
}
