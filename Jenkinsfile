pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker image build --tag sample:sample - < Dockerfile'
                sh 'docker create sample'
                sh 'ls'
            }
        }
        stage('Test') {
            steps {
                sh 'microscope docker -pkgdb /var/microscope/pkg.csv sample'
            }
        }
    }
}
