pipeline {
//   agent any
    agent { node { label 'workstation' } }

    stages {
        stage('compile') {
            steps {
                echo 'Hello World'
            }
        }


    }

    post {
        always {
            echo 'I will always say Hello again!'
            error 'hello world'
        }
    }
}