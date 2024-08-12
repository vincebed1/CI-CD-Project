pipeline {
    agent any

    environment {
        GIT_REPO_URL = 'https://github.com/vincebed1/CI-CD-Project.git'
        BRANCH = 'master'
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout the source repo from SCM
                git branch: "${BRANCH}", url: "${GIT_REPO_URL}"
            }
        }
        stage('Build') {
            steps {
                // Compile the Java code
                sh 'javac CI_CD.java'
            }
        }
        stage('Deploy') {
            steps {
                // Run the compiled Java class
                sh 'java CI_CD'
            }
        }
        stage('Debug Environment') {
            steps {
                // Print Java environment details
                sh 'echo $JAVA_HOME'
                sh 'java -version'
            }
        }
    }

    post {
        always {
            echo 'Cleaning up...'
            // Add any cleanup steps here, if needed
        }
        success {
            echo 'Build and deploy successful!'
        }
        failure {
            echo 'Build or deploy failed.'
        }
    }
}
