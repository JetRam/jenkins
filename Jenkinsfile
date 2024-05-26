pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Running Build Task'
                echo 'Maven Tool:'
                echo 'Java Project Automation Tool'
            }
        }
        stage('Test') {
            steps {
                echo 'Running Unit Testing'
                echo 'Checking Individual Components Running'
                echo 'Mocha/Chai Unit Testing'
                echo 'Integration Testing'
                echo 'Code Working As Expected'
                echo 'Postman:'
                echo 'API Testing'
            }
            post {
                always {
                    emailext(
                        to: 'djethroramos@gmail.com',
                        subject: "Jenkins Build: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                        body: """<p>Completed 'Unit and Integration Test'""",
                        attachLog: true
                    )
                }
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Running Code Analysis'
                echo 'Checking for code quality'
                echo 'ESLint:'
                echo 'Javascript Code Tool'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Running Security Scan'
                echo 'Veracode'
                echo 'Analyzing source code for security'
                echo 'Identifying code errors'
            }
            post {
                always {
                    emailext(
                        to: 'djethroramos@gmail.com',
                        subject: "Jenkins Build: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                        body: """Done with the Security Scan with Build Log""",
                        attachLog: true
                    )
                }
            }
        }
        stage('Deploy to staging') {
            steps {
                echo 'Deploying to Stagig'
                echo 'AWS EC2 deploy:'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Integrating Tests on Staging'

            }
        }
        stage('Deploy to production') {
            steps {
                echo 'Deploying to production'
            }
        }
    }
}