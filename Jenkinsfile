pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                //Checkout the source repo from scm
                git 'Building..'
            }
        }
        stage('Test') {
            steps {
                //Checkout the source repo from scm
                git 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
