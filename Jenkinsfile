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

        stage('Build') {
            steps {
                input message: 'Do you want to continue?', ok: 'Yes, deploy'

            }
        }

        stage('test') {
            steps {
                echo 'Running tests'
                sh 'date'

            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploing the app'
                sh 'hostname'
                sh 'ip r'

            }

        }
    }  
}
