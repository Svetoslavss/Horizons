pipeline {
    agent any
        stage('Restore dependencies') {
            steps {
                bat "dotnet restore"
            }
        }
        stage('Build') {
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
