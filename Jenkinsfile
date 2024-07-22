pipeline {
    agent { label 'Jenkins-agent' }
    tools {
        maven 'MAVEN'
    }
    stages {
        stage('verify tooling') {
            steps {
                sh 'java --version'
                sh 'mvn -v'
            }
        }
        stage('testing'){
            steps {
                sh 'mvn mvn clean test -Dsurefire.suiteXmlFiles=${suiteFileLocal}'
                echo 'running test automation'
            }
        }
        stage('deploy'){
            steps {
                echo 'deploying to staging environment'

            }
        }
    }
    post {
        always {
            sh 'sending message to slack'
        }
    }
}