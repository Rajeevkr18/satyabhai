pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the code from your updated GitHub repo
                    git branch: 'main', url: 'https://github.com/Rajeevkr18/satyabhai.git'
                }
            }
        }

        stage('Build') {
            steps {
                echo 'Building HTML project...'
                // Add your HTML/CSS/JS build steps here if needed
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying the project...'
                // Example: Add steps to deploy the static site
                // sh 'scp -r * user@your-server:/var/www/html'
                // or use GitHub Pages, Netlify CLI, etc.
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests (if any)...'
                // Add test commands here if applicable
            }
        }
    }

    post {
        success {
            echo '✅ Build and deployment successful!'
        }
        failure {
            echo '❌ Build or deployment failed!'
        }
    }
}
