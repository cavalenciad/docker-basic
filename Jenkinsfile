pipeline {
    agent any

    tools {
        dotnetsdk 'dotnet-9'
    }

    stages {
        stage('Build') {
            steps {
                dir('10-net9-remix-pg-env/Backend') {
                    echo 'Restoring dependencies...'
                    sh 'dotnet restore'
                }
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