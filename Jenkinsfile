pipeline {
    agent 'Jenkins-agent'
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
    }
}