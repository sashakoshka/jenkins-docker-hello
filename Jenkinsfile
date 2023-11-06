pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                script {
                    sh 'docker image build --tag sample:sample - < Dockerfile'
                    def containerName = sh(script: 'docker create sample:sample --name sample', returnStdout: true).trim()
                    println("container name: ${containerName}")
                    env.CONTAINER_NAME = containerName
                }
            }
        }
        stage('Test') {
            steps {
                sh 'microscope docker -pkgdb /var/microscope/pkg.csv ${CONTAINER_NAME}'
            }
        }
    }
}
