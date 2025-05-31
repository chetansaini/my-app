pipeline {
    agent any

    tools {
        nodejs "NodeJS 16"  // You must install and name this version in Jenkins
    }

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/chetansaini/my-app.git', branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }


        stage('Build (Optional)') {
            steps {
                echo 'Build step can go here if needed.'
            }
        }
    }

    post {
        success {
            echo 'Build succeeded!'
        }
        failure {
            echo 'Build failed!'
        }
    }
}
