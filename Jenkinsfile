pipeline {
    agent any

    stages {
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