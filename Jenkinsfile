node {
    checkout scm

    // deploy env dev
    stage("Build") {
        docker.image('composer:latest').inside('-u root') {
            sh 'php -v'
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