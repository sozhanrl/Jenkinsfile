pipeline {
    agent any

    stages {
        stage('Workspace Cleanup') {
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
