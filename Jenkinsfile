pipeline {
    agent any

    stages {
        stage('Environment Setup') {
            steps {
                echo "Running pipeline on branch: ${env.BRANCH_NAME}"
                // Copy .env.example to .env if .env doesn't exist
                sh 'cp -n .env.example .env || true'
            }
        }

        stage('Dependencies') {
            steps {
                sh 'composer install --no-interaction --prefer-dist'
            }
        }

        stage('Tests') {
            steps {
                sh 'php artisan key:generate'
                sh 'php artisan test'
            }
        }

        stage('Finished') {
            steps {
                echo "Successfully tested branch: ${env.BRANCH_NAME}"
            }
        }
    }
}