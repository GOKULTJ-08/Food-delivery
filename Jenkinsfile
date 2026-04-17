pipeline {
    agent any

    stages {
        stage('Clone') {
            steps {
                git 'https://github.com/GOKULTJ-08/food-delivery-devops.git'
            }
        }

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t food-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 food-app'
            }
        }
    }
}
