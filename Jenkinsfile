pipeline {
    agent any

    stages {
        stage('git to jenkins') {
            steps {
                checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[credentialsId: 'b4182c20-63b1-475c-be7e-5a803d886977', url: 'https://github.com/Hemanthsrk/javaprojectown.git']])
            }
        }
        stage('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
