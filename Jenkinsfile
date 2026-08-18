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
                // Windows batch command using %DATE% and %TIME%
                bat 'echo Build #%BUILD_NUMBER% executed on %DATE% %TIME% > build-info.txt'
            }
        }
    }
   
    post {
        success {
            echo 'Build successful! Ready for release.'
        }
    }
}
