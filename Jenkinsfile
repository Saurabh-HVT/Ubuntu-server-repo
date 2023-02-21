pipeline {
    agent any
    stages {
        stage('Git clone') {
            steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Saurabh-HVT/Ubuntu-server-repo.git']])
            }
        }
        stage('Maven Build') {
            steps {
               sh 'mvn pakage'
            }
        }
        stage('Maven Deploy') {
            steps {
               echo "Deploying war file to server"
            }
        }
    }
}
