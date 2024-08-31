pipeline {
//   agent any
    agent { node { label 'workstation' } }
    environment {
    ssh = credentials('centos-ssh')
    }
    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
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
    env ssh
}