node {
    checkout scm

    // deploy env dev
    stage("Build") {
        docker.image('shippingdocker/php-composer:latest').inside('-u root') {
            sh 'rm composer.lock'
            sh 'composer install'
        }
    }

    // Testing
    stage("Testing") {
        docker.image('ubuntu').inside('-u root') {
            sh 'echo "Ini adalah test"'
        }
    }
}