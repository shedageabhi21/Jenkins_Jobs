pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Code checkout completed'
            }
        }

        stage('Build') {
            steps {
                echo 'Building application'
                sh 'ls -l'
            }
        }

        stage('Approval') {
            steps {
                input message: 'Do you want to continue?', ok: 'Yes, deploy'
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests'
                sh 'date'
            }
        }

        stage('Approval2') {
            steps {
                script {
                    def userInput = input(
                        message: 'Approve deployment?',
                        parameters: [
                            string(name: 'VERSION', defaultValue: '1.0', description: 'Version to deploy'),
                            booleanParam(name: 'CONFIRM', defaultValue: true, description: 'Confirm deployment?')
                        ]
                    )
                    echo "User entered VERSION: ${userInput['VERSION']}"
                    echo "User confirmed: ${userInput['CONFIRM']}"
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the app'
                sh 'hostname'
                sh 'ip r'
            }
        }
    }
}
