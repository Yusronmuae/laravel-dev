pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git 'https://github.com/Yusronmuae/laravel-dev.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    docker.image('composer:2').inside {
                        sh 'composer install'
                    }
                }
            }
        }

        stage('Build') {
            steps {
                sh 'php artisan key:generate'
            }
        }
    }
}