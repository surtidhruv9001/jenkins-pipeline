pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building...'
                // Optionally, use Maven or Gradle here if you have a specific build tool
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests...'
                // Use test automation tools like JUnit for Java, or pytest for Python
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Running Code Analysis...'
                // Example: Use tools like SonarQube or CheckStyle for static code analysis
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Running Security Scan...'
                // Example: Use tools like OWASP Dependency Check, Snyk, or Bandit for security scanning
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging...'
                // Example: Deploy to AWS EC2, Heroku, or any other staging environment
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging...'
                // Integration testing on the staging environment
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                // Deploy the app to the production environment (e.g., AWS, Heroku, etc.)
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
            // Optional: Send a success email or notification here
        }
        failure {
            echo 'Pipeline failed!'
            // Optional: Send a failure email or notification here
        }
    }
}
post {
    success {
        mail to: 'surtidhruv9001aus@gmail.com',
             subject: "Jenkins Pipeline Successful: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
             body: "The Jenkins pipeline ${env.JOB_NAME} build #${env.BUILD_NUMBER} was successful."
    }
    failure {
        mail to: 'surtidhruv9001aus@gmail.com',
             subject: "Jenkins Pipeline Failed: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
             body: "The Jenkins pipeline ${env.JOB_NAME} build #${env.BUILD_NUMBER} has failed."
    }
}


post {
    success {
        mail to: 'surtidhruv9001aus@gmail.com',
             subject: "Jenkins Pipeline Successful: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
             body: "The Jenkins pipeline ${env.JOB_NAME} build #${env.BUILD_NUMBER} was successful."
    }
    failure {
        mail to: 'surtidhruv9001aus@gmail.com',
             subject: "Jenkins Pipeline Failed: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
             body: "The Jenkins pipeline ${env.JOB_NAME} build #${env.BUILD_NUMBER} has failed."
    }
}

