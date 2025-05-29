pipeline {
    agent any

    tools {
        dotnetsdk 'dotnet-9'
    }

    stages {
        stage('Backend - Restore') {
            steps {
                dir('10-net9-remix-pg-env/Backend') {
                    echo 'Restoring dependencies...'
                    sh 'dotnet restore'
                }
            }
        }
        stage('Backend- Test') {
            steps {
                dir('10-net9-remix-pg-env/Backend') {
                    echo 'Running tests...'
                    sh 'dotnet test --no-build --verbosity normal'
                }
            }
        }
        stage('Backend - Build') {
            steps {
                dir('10-net9-remix-pg-env/Backend') {
                    echo 'Building the project...'
                    sh 'dotnet build --configuration Release --no-restore'
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