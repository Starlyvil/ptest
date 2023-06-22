pipeline {
    agent any
    stages('my-stage'){
        stage('Build') {
            steps {
                input {
                    message "Should we continue?"
                    ok "Yes, we should."
                    submitter "starlyvil"
                    parameters {
                        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
                    }
                }
                sh "echo Building code....."
                sh "whoami"
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
