pipeline {
    agent any
    tools {maven 'M3'}
    stages {
        stage('Checkout') {
            steps {
                echo 'Checking out code'
                git branch: 'main' , url: 'https://github.com/sujit-das/SpringPetClinic.git'
            }
        }
        stage('Build') {
            steps {
                echo "Building code"
                sh 'mvn compile'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing code'
                sh 'mvn test'
            }
        }
        stage ('Package') {
            steps {
                echo 'Packaging change'
                sh 'mvn package'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying change'
            }
        }
    }
}
