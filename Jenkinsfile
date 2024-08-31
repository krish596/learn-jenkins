pipeline {
//   agent any
    agent { node { label 'workstation' } }
    environment {
        Test_Url = "google.com"
        SSH = credentials('centos-ssh')
    }

    options {
        ansiColor('xterm')
    }

    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }

    triggers { pollSCM('*/1 * * * *') }
    //

    tools {
        maven 'maven'
    }
    input {
        message "Should we continue?"
        ok "Yes, we should."

    }
    stages {
        stage('compile') {
            steps {
               // echo 'Hello World'
               echo Test_Url
               echo SSH
               sh 'env'
               sh 'ansible -i 172.31.44.244, all -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
            }
        }


    }

    post {
        always {
            echo 'post'
            // I will always say Hello again

            // hello world
        }
    }
}