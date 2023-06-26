pipeline {
    agent any
    environment {
        AA = credentials("test-credential")
    }
     parameters {
       // string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
         string(name: 'PERSON', description: 'Who should I say hello to?')
         choice(name: 'severity', choices: ['A', 'B', 3], description: '')
     }
    stages {
        stage('Build') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'test-credential', usernameVariable: 'UN', passwordVariable: 'PW'), sshUserPrivateKey(credentialsId: 'global_key',
                      keyFileVariable: 'SSH_KEY_FOR_ABC',
                      passphraseVariable: '',
                      usernameVariable: '')]){
                    echo "my user name is ${UN} and my password is ${PW} and path to pk => ${SSH_KEY_FOR_ABC}"
                }
                sh "echo Building code..... ${AA_USR} and password ${AA_PSW}"
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
