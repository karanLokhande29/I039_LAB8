pipeline {
    agent any

    stages {
        stage('Pull from Git') {
            steps {
                // Jenkins automatically checks out code when using "Pipeline script from SCM", 
                // but this explicit step fulfills the "Pull" stage requirement visually.
                git branch: 'main', url: 'https://github.com/karanLokhande29/I039_LAB8'
            }
        }
        stage('Build') {
            steps {
                bat 'Build.bat'
            }
        }
        stage('Test') {
            steps {
                bat 'Test.bat'
            }
        }
        stage('Deploy') {
            steps {
                bat 'Deploy.bat'
            }
        }
    }
}
