pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building project...'
            }
        }
    }

    post {
        success {
            echo 'Build was SUCCESSFUL ✅'
        }
        failure {
            echo 'Build FAILED ❌'
        }
        always {
            echo 'Post-build actions completed.'
        }
    }
}
