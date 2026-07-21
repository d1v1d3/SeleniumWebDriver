pipeline {
    agent any
    stages {
        stage('Restore') {
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build') {
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Test Project 2') { 
            steps {
                bat 'dotnet test TestProject2 --no-build --verbosity normal'
            }
        }
        stage('Test Project 3') { 
            steps {
                bat 'dotnet test TestProject3 --no-build --verbosity normal'
            }
        }
        stage('Test Project 1') { 
            steps {
                bat 'dotnet test TestProject1 --no-build --verbosity normal'
            }
        }
    }
}