pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker iamge build - < Dockerfile'
                sh 'ls'
            }
        }
    }
}
