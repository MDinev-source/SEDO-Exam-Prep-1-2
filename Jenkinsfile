pipeline {
    agent any

    stages {
        stage('Restore the dependencies') {
            when {
                anyOf {
                    branch 'main'
                    branch 'develop'
                }
            }
            steps {
                bat 'dotnet restore'
            }
        }
        stage('Build Application') {
            when {
                anyOf {
                    branch 'main'
                    branch 'develop'
                }
            }
            steps {
                bat 'dotnet build --no-restore'
            }
        }
        stage('Test Application') {
            when {
                anyOf {
                    branch 'main'
                    branch 'develop'
                }
            }
            steps {
                bat 'dotnet build --no-restore'
            }
        }
    }
}
