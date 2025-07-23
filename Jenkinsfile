pipeline {
    agent any
    environament {
        IMAGE_NAME= 'my-java-app'
    }
    stages {
        stage('Build Java App') {
            steps{
                echo 'Building Java App...'
                sh 'javac src/Hello.java'
            }
        }
        stage('Build Docker Image') {
            steps{
                echo 'Building Docker Image...'
                sh 'docker build -t \$IMAGE_NAME .'
            }
        }
         stage('Run Docker Container') {
            steps{
                echo 'Running Docker Container...'
                sh'docker run --rm \$IMAGE_NAME'
            }
         }
    
    }
}
