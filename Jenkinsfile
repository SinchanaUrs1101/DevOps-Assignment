pipeline {
    agent any

    stages {

        stage('Clone') {
            steps {
                git 'https://github.com/SinchanaUrs1101/DevOps-Assignment.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-app ./backend'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 8000:8000 devops-app'
            }
        }
    }
}