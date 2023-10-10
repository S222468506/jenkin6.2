pipeline {
    agent any

    stages {
        stage('Delay Stage') {
            steps {
                script {
                    echo 'Starting Delay Stage'
                    sleep 5
                    echo 'Delay completed'
                }
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully'
        }
        failure {
            echo 'Pipeline failed'
        }
    }
}
