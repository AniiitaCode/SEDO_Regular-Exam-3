pipeline {

    agent any

    stages {
        stage("Restore the dependecies") {
            steps {
                bat 'dotnet restore'
            }
        }
        
        stage("Build the application") {
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        
        stage("Run the test") {
            steps {
                bat 'dotnet test --no-build --verbosity normal'
            }
        }
    }
}
