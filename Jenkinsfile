pipeline {
    agent any

    stages {
        stage('Clean Workspace') {
            steps {
                deleteDir()
            }
        }

        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }
    }
}
