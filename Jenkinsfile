pipeline {
    agent any

    stages {
        stage('Environment Setup') {
            steps {
                echo "Running pipeline on branch: ${env.BRANCH_NAME}"
                sh 'echo "Simulating .env setup"'
            }
        }

        stage('Dependencies') {
            steps {
                sh 'echo "Simulating composer install"'
            }
        }

        stage('Tests') {
            steps {
                sh 'echo "Simulating php artisan test"'
            }
        }

        stage('Finished') {
            steps {
                echo "Pipeline execution finished successfully for ${env.BRANCH_NAME}!"
            }
        }
    }
}