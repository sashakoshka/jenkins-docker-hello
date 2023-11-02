pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker image build --tag sample:sample - < Dockerfile'
                sh 'ls'
            }
        }
        stage('Test') {
            steps {
                sh 'microscope docker -pkgdb /home/opc/pkg.csv sample'
            }
        }
    }
}
