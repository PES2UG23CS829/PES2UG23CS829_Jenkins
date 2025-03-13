pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'g++ -o PES2UG23CS829-2 man.cpp'
                echo 'Build stage completed successfully'
            }
        }

        stage('Test') {
            steps {
                sh './PES2UG23CS829-2'
                echo 'Test stage completed successfully'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deployment stage completed successfully'
                echo 'Deployed the application'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
        success {
            echo 'Pipeline executed successfully'
        }
    }
}
