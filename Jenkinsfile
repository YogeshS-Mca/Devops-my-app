pipeline {
    agent any

    stages {

       stage('Clone Repository') {
    steps {
        git branch: 'main', url: 'https://github.com/YogeshS-Mca/Devops-my-app.git'
    }
}

        stage('Build Docker Image') {
            steps {
                sh 'docker build -t devops-my-app .'
            }
        }

        stage('Run Container') {
            steps {
                sh 'docker run -d -p 5000:5000 devops-my-app'
            }
        }

    }
}
