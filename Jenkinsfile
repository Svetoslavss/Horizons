pipeline {
    agent any
    stages {
        stage('Checkout repository') {
            steps {
                checkout scm
            }
        }
        stage('Restore dependencies') {
            steps {
                bat "dotnet restore"
            }
        }
        stage('Build the app') {
            steps {
                bat "dotnet build --no-restore --verbosity normal"
            }
        }
     
        stage('Test') {
            steps {
                bat "dotnet test --no-build --verbosity normal"
            }
        }
    }
}
