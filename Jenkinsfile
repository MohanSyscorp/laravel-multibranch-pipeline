pipeline {
    agent any

    stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/your-username/laravel-auto-build.git'
            }
        }

        stage('Dependencies') {
            steps {
                sh 'composer install'
            }
        }

        stage('Tests') {
            steps {
                sh 'php artisan test'
            }
        }

        stage('Finished') {
            steps {
                echo 'Build Successful'
            }
        }
    }
}