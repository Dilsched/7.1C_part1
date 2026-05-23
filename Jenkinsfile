pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                echo '========== Stage 1: Build =========='
                echo 'Tool: Maven'
                echo 'Task: Building the code using Maven to compile and package the application.'
                echo 'Command that would run: mvn clean package'
            }
        }

        stage('Unit and Integration Tests') {
            steps {
                echo '========== Stage 2: Unit and Integration Tests =========='
                echo 'Tools: JUnit (unit tests), Selenium (integration tests)'
                echo 'Task: Running unit tests to verify individual components function correctly.'
                echo 'Task: Running integration tests to verify all components work together.'
            }
        }

        stage('Code Analysis') {
            steps {
                echo '========== Stage 3: Code Analysis =========='
                echo 'Tool: Checkstyle'
                echo 'Task: Analysing the code to ensure it meets industry coding standards.'
            }
        }

        stage('Security Scan') {
            steps {
                echo '========== Stage 4: Security Scan =========='
                echo 'Tool: OWASP Dependency-Check'
                echo 'Task: Scanning dependencies for known CVEs and security vulnerabilities.'
            }
        }

        stage('Deploy to Staging') {
            steps {
                echo '========== Stage 5: Deploy to Staging =========='
                echo 'Tool: AWS CLI / AWS CodeDeploy'
                echo 'Task: Deploying the application to a staging AWS EC2 instance.'
            }
        }

        stage('Integration Tests on Staging') {
            steps {
                echo '========== Stage 6: Integration Tests on Staging =========='
                echo 'Tool: Postman / Newman'
                echo 'Task: Running integration tests on the staging environment.'
            }
        }

        stage('Deploy to Production') {
            steps {
                echo '========== Stage 7: Deploy to Production =========='
                echo 'Tool: AWS CLI / AWS CodeDeploy'
                echo 'Task: Deploying the verified application to the production AWS EC2 instance.'
            }
        }

    }

    post {
        success { echo 'All 7 stages completed successfully!' }
        failure { echo 'Pipeline failed. Check the console output.' }
    }
}
