pipeline {
//   agent any
    agent { node { label 'workstation' } }
    environment {
        Test_Url = "google.com"
        SSH = credentials('centos-ssh')
    }
    stages {
        stage('compile') {
            steps {
               // echo 'Hello World'
               echo Test_Url
               echo SSH
               sh 'env'
               sh 'ansible -i 172.31.44.244, -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
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