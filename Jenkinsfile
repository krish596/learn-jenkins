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