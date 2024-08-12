pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source repo from SCM
                git 'https://github.com/vincebed1/CI-CD-Project.git'
            }
        }
        stage('Build') {
            steps {
                // Compile the Java code
                sh 'javac CI_CD.java'
            }
        }
        stage('Deploy') {
            //Run the compiled Java class
            steps {
                sh 'java CI_CD'
            }
        }
    }
}
