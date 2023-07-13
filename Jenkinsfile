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

        stage('deploy') {
            steps {
                deploy adapters: [tomcat9(credentialsId: '85003a7b-e5db-465c-add0-10695347434e', path: '', url: 'localhost:8080')], contextPath: '/', onFailure: false, war: '**/*.war'
            }
        }
    }
}