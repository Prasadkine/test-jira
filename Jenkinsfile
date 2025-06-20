pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Building....."
                // Run your build commandsh
            }
        }
        stage('Deploy') {
            steps {
                echo "Deploying...."
                // Run your deployment steps
            }
        }
        stage('Notify Jira') {
            steps {
                script {
                    jiraSendBuildInfo site: 'https://kine.atlassian.net'
                    jiraSendDeploymentInfo site: 'https://kine.atlassian.net'
                }
            }
        }
    }
}
