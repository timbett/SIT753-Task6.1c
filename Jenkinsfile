pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                script {
                    // Build the code using Maven
                    sh 'mvn clean package'
                }
            }
            post {
                always {
                    echo "Build stage completed."
                }
                success {
                    echo "Build stage executed successfully."
                }
                failure {
                    echo "Build stage failed."
                }
            }
        }
        stage("Unit and Integration Tests") {
            steps {
                script {
                    // Run unit tests and integration tests
                    sh 'run_unit_tests.sh'
                    sh 'run_integration_tests.sh'
                }
            }
            post {
                always {
                    echo "Unit and Integration Tests stage completed."
                }
                success {
                    echo "Unit and Integration Tests stage executed successfully."
                }
                failure {
                    echo "Unit and Integration Tests stage failed."
                }
            }
        }
        stage("Code Analysis") {
            steps {
                script {
                    // Integrate a code analysis tool (e.g., SonarQube) to analyze the code
                    sh 'run_code_analysis.sh'
                }
            }
            post {
                always {
                    echo "Code Analysis stage completed."
                }
                success {
                    echo "Code Analysis stage executed successfully."
                }
                failure {
                    echo "Code Analysis stage failed."
                }
            }
        }
        stage("Security Scan") {
            steps {
                script {
                    // Perform security scan using a tool (e.g., SonarQube) to identify vulnerabilities
                    sh 'run_security_scan.sh'
                }
            }
            post {
                always {
                    echo "Security Scan stage completed."
                }
                success {
                    echo "Security Scan stage executed successfully."
                }
                failure {
                    echo "Security Scan stage failed."
                }
            }
        }
        stage("Deploy to Staging") {
            steps {
                script {
                    // Deploy the application to a staging server (e.g., AWS EC2 instance)
                    sh 'deploy_to_staging.sh'
                }
            }
            post {
                always {
                    echo "Deploy to Staging stage completed."
                }
                success {
                    echo "Deploy to Staging stage executed successfully."
                }
                failure {
                    echo "Deploy to Staging stage failed."
                }
            }
        }
        stage("Integration Tests on Staging") {
            steps {
                script {
                    // Run integration tests on the staging environment
                    sh 'run_integration_tests_on_staging.sh'
                }
            }
            post {
                always {
                    echo "Integration Tests on Staging stage completed."
                }
                success {
                    echo "Integration Tests on Staging stage executed successfully."
                }
                failure {
                    echo "Integration Tests on Staging stage failed."
                }
            }
        }
        stage("Deploy to Production") {
            steps {
                script {
                    // Deploy the application to a production server (e.g., AWS EC2 instance)
                    sh 'deploy_to_production.sh'
                }
            }
            post {
                always {
                    echo "Deploy to Production stage completed."
                }
                success {
                    echo "Deploy to Production stage executed successfully."
                }
                failure {
                    echo "Deploy to Production stage failed."
                }
            }
        }
    }
    post {
        always {
            echo "Pipeline completed."
        }
        success {
            echo "Pipeline executed successfully."
        }
        failure {
            echo "Pipeline execution failed."
        }
    }
}
