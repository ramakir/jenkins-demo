pipeline {
    agent none

    stages {

        stage('Checkout') {
            agent { label 'built-in' }

            steps {
                checkout scm
                stash name: 'source', includes: '**/*'
            }
        }

        stage('Agent1 Build') {
            agent { label 'agent1' }

            steps {
                unstash 'source'
                sh 'hostname'
                sh 'ls -la'
                sh 'java -version'
                sh 'git --version'
            }
        }

        stage('Agent2 Test') {
            agent { label 'agent2' }

            steps {
                unstash 'source'
                sh 'hostname'
                sh 'uptime'
            }
        }
    }
}
