fpipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker image build --tag sample:sample - < Dockerfile'
                def containerName = sh('docker create sample:sample --name sample', returnStdout: true).trim()
                println("container name: ${containerName}")
                env.CONTAINER_NAME = containerName
            }
        }
        stage('Test') {
            steps {
                sh 'microscope docker -pkgdb /var/microscope/pkg.csv ${containerName}'
            }
        }
    }
}
