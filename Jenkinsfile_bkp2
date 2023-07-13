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
        stage ('test') {
            steps {
                echo 'this is artifact test steps'
            }
        }
        stage ('publish') {
            steps {
                echo 'this is artifact publish steps'
            }
        }
        stage ('deploy') {
            steps {
                echo 'this is artifact deploy steps'
            }
        }
    }
}