pipeline {
    agent {
        node {
            label 'Agent1' // Corrected syntax: 'label' instead of '='
        }
    }
    environment {
            GREETINGS = 'hello worls'
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                   echo 'hwre is dhell'
                   env
                """
            }
        }
    }
    post {
        always {
            echo 'will run'
        }
    }
}
