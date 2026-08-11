pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo 'Compiling application...'
            }
        }

        stage('Test') {
            steps {
                echo 'Running unit tests... Pass!'
            }
        }

        stage('Package') {
            steps {
                sh 'echo "Build Number: ${BUILD_NUMBER}" > build-info.txt'
                sh 'echo "Build executed on $(date)" >> build-info.txt'
            }
        }
    }

    post {
        success {
            echo 'Build successful! Ready for release.'
        }
    }
}