pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clones your specific GitHub repository
                git branch: 'main', url: 'https://github.com'
            }
        }
        stage('Build') {
            steps {
                echo 'Building your application...'
                // Add your build commands here (e.g., sh 'npm run build' or sh './gradlew build')
            }
        }
        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test commands here (e.g., sh 'npm test' or sh './gradlew test')
            }
        }
    }
    
    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed. Please check the logs.'
        }
    }
}
