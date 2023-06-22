pipeline {
    agent any
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
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
