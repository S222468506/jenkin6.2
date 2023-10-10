pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Executing Build Stage'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Executing Unit and Integration Tests Stage'
            }
            post {
                success {
                    mail to: 's222311692@deakin.edu.au',
                         subject: 'Successful Unit and Integration Tests: ${currentBuild.fullDisplayName}',
                         body: 'Unit and Integration Tests completed successfully. Check the attached logs for more details.'
                }
                failure {
                    mail to: 's222311692@deakin.edu.au',
                         subject: 'Failed Unit and Integration Tests: ${currentBuild.fullDisplayName}',
                         body: 'Check the attached logs for more details.'

                }
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Executing Code Analysis Stage'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Executing Security Scan Stage'
            }
            post {
                success {
                    mail to: 's222311692@deakin.edu.au',
                         subject: 'Successful Security Scan: ${currentBuild.fullDisplayName}',
                         body: 'Security Scan completed successfully. Check the attached logs for more details.'

                }
                failure {
                    mail to: 's222311692@deakin.edu.au',
                         subject: 'Failed Security Scan: ${currentBuild.fullDisplayName}',
                         body: 'Check the attached logs for more details.'

                }
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Executing Deploy to Staging Stage'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Executing Integration Tests on Staging Stage'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Executing Deploy to Production Stage'
            }
        }
    }
}
