pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                //Checkout the source repo from scm
                git 'https://github.com/vincebed1/CI-CD-Project.git'
            }
        }
        stage('Build') {
            steps {
                //Build the java code
                java 'CI_CD.java'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
