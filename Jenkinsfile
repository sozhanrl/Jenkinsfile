pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                bat 'javac HelloWorld.java'
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }

    post {
        success {
            echo 'CI Pipeline completed successfully.'
        }
        failure {
            echo 'Build failed due to compilation error!'
        }
    }
}
