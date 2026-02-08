pipeline {
    agent any

    triggers {
        pollSCM('* * * * *')   // Checks Git every minute
    }

    stages {

        stage('Checkout Code') {
            steps {
                echo 'Pulling latest code from Git...'
                checkout scm
            }
        }

        stage('Compile') {
            steps {
                echo 'Compiling source code...'
                sh 'javac HelloWorld.java'     // For Linux/Mac
                // For Windows use: bat 'javac HelloWorld.java'
            }
        }

        stage('Archive Artifacts') {
            steps {
                echo 'Archiving compiled files...'
                archiveArtifacts artifacts: '*.class', fingerprint: true
            }
        }
    }

    post {
        failure {
            echo 'Build failed due to compilation error!'
        }
        success {
            echo 'CI Pipeline completed successfully.'
        }
    }
}
