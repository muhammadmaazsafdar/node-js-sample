pipeline {
    agent any

    tools {
        nodejs "NodeJS"
    }

    stages {
        stage('Clone Repository') {
            steps {
                git 'https://github.com/muhammadmaazsafdar/node-js-sample.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Run Tests') {
            steps {
                sh 'npm test'
            }
        }

        stage('Start Application') {
            steps {
                sh 'nohup npm start &'
                echo "Application is running on http://<your-azure-ip>:3000"
            }
        }
    }
}
