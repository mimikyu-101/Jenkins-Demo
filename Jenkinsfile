pipeline {
    agent any

    parameters {
        booleanParam(name: 'RUN_TESTS', defaultValue: true, description: 'Run test stage?')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }

        stage('Test') {
            when {
                expression { params.RUN_TESTS }
            }
            steps {
                echo 'Testing..'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying..'
            }
        }
    }
}
