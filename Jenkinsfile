pipeline {
    agent {
        node {
            label 'Agent1' // Corrected syntax: 'label' instead of '='
        }
    }
    environment {
            GREETINGS = 'hello worls'
    }
    parameters {
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')

        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')

        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')

        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')

        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing....'
            }
        }
        stage('Example') {
            steps {
                echo "Hello ${params.PERSON}"

                echo "Biography: ${params.BIOGRAPHY}"

                echo "Toggle: ${params.TOGGLE}"

                echo "Choice: ${params.CHOICE}"

               
            }
        }
        stage('Deploy') {
            steps {
                sh """
                   echo 'hwre is dhell'
                echo '$GREETINGS'
                echo 'printed'
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

