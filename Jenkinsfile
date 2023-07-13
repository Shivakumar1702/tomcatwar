pipeline {
    agent any
    stages {
        stage ('Init') {
            steps {
                echo 'this is the git checkout step'
            }
        }

        stage ('build') {
            steps {
                echo 'this is the project build step'
            }
        }
        stage ('publish') {
            steps {
                echo 'this is artifact publish steps'
            }
        }
    }
}