pipeline {
    agent any

    triggers {
        pollSCM('H/2 * * * *')
    }

    stages {
        stage('Build') {
            steps {
                echo 'Task: Compile and package the code into a deployable artefact'
                echo 'Tool: Maven (mvn clean package)'
            }
        }
        stage('Unit and Integration Tests') {
            steps {
                echo 'Task: Run unit tests to check each function works as expected'
                echo 'Task: Run integration tests to check the components work together'
                echo 'Tools: JUnit (unit tests), Selenium / Postman (integration tests)'
            }
        }
        stage('Code Analysis') {
            steps {
                echo 'Task: Analyse the code to make sure it meets industry standards'
                echo 'Tool: SonarQube (via the SonarQube Scanner plugin for Jenkins)'
            }
        }
        stage('Security Scan') {
            steps {
                echo 'Task: Scan the code and its dependencies for known vulnerabilities'
                echo 'Tool: OWASP Dependency-Check (or Snyk)'
            }
        }
        stage('Deploy to Staging') {
            steps {
                echo 'Task: Deploy the application to a staging server'
                echo 'Tool: AWS CodeDeploy to an AWS EC2 staging instance'
            }
        }
        stage('Integration Tests on Staging') {
            steps {
                echo 'Task: Run integration tests on staging to confirm it works in a production-like environment'
                echo 'Tool: Selenium / Postman (Newman)'
            }
        }
        stage('Deploy to Production') {
            steps {
                echo 'Task: Deploy the application to the production server'
                echo 'Tool: AWS CodeDeploy to an AWS EC2 production instance'
            }
        }
    }
}
