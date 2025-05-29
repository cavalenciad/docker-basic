pipeline {
    agent any

    tools {
        dotnetsdk 'dotnet-9'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                sh 'dotnet --version'
                // Add your build steps here
            }
        }
        stage('Test') {
            steps {
                echo 'Hola mundo!...'
                echo 'Running tests...'
                // Add your test steps here
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                // Add your deployment steps here
            }
        }
    }

    post {
        always {
            echo 'This will always run after the stages.'
            // Add any cleanup or notification steps here
        }
    }
}