pipeline {

    agent {
        label 'linux'
    }

    stages {

        stage('Who Am I') {
            steps {
                sh 'hostname'
                sh 'whoami'
            }
        }

        stage('Java Version') {
            steps {
                sh 'java -version'
            }
        }

        stage('Workspace') {
            steps {
                sh 'pwd'
                sh 'ls -la'
            }
        }
    }
}
