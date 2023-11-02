pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker image build - < Dockerfile'
                sh 'ls'
            }
        }
    }
}
