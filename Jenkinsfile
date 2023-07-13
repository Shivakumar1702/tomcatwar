pipeline {
    agent any
    stages {

        stage('git checkout') {
            steps {
                checkout scmGit(branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Shivakumar1702/tomcatwar.git']])
            }
        }

        stage('maven build') {
            steps {
                bat 'mvn -f myartifact/pom.xml clean package'
            }
        }

        stage('archive artifacts') {
            steps {
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
            }
        }
    }
}