pipeline {
    agent any

    environment {
        // Set environment variables here if necessary
        EMAIL_RECIPIENT = 'surtidhruv9001aus@gmail.com'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building the application...'
                // Example: Integrate with a build tool like Maven or Gradle
                // sh 'mvn clean package'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo 'Running Unit and Integration Tests...'
                // Example: Use JUnit or pytest to run unit tests
                // sh 'mvn test'
            }
        }

        stage('Code Analysis') {
            steps {
                echo 'Running Code Analysis...'
                // Example: Use SonarQube for code analysis
                // sh 'sonar-scanner'
            }
        }

        stage('Security Scan') {
            steps {
                echo 'Running Security Scan...'
                // Example: Use OWASP Dependency Check for security scanning
                // sh 'dependency-check.sh --project Jenkinsfile --out .'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo 'Deploying to Staging...'
                // Example: Deploy to a staging environment such as an AWS EC2 instance
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo 'Running Integration Tests on Staging...'
                // Example: Running tests in the staging environment
            }
        }

        stage('Deploy to Production') {
            steps {
                echo 'Deploying to Production...'
                // Example: Deploy to production, e.g., AWS EC2
            }
        }
    }

    post {
        success {
            echo 'Pipeline succeeded!'
            mail to: "$EMAIL_RECIPIENT",
                 subject: "Jenkins Pipeline Successful: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
                 body: "The Jenkins pipeline ${env.JOB_NAME} build #${env.BUILD_NUMBER} was successful.\n\nCheck console output at ${env.BUILD_URL} to view the results."
        }
        failure {
            echo 'Pipeline failed!'
            mail to: "$EMAIL_RECIPIENT",
                 subject: "Jenkins Pipeline Failed: ${env.JOB_NAME} Build #${env.BUILD_NUMBER}",
                 body: "The Jenkins pipeline ${env.JOB_NAME} build #${env.BUILD_NUMBER} has failed.\n\nCheck console output at ${env.BUILD_URL} to diagnose the problem."
        }
    }
}

