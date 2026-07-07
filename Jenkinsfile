pipeline {
    agent none

    stages {

        stage('Checkout') {
            agent { label 'built-in' }   // or your controller label
            steps {
                checkout scm
            }
        }

        stage('Agent1 Build') {
            agent { label 'agent1' }
            steps {
                sh 'hostname'
		sh 'java -version'
		sh 'git --version'
            }
        }
        stage('Agent2 Test') {
            agent { label 'agent2' }

            steps {
                sh 'hostname'
                sh 'uptime'
            }
        }
    }
}
