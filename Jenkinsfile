pipeline {
    agent {
        label 'agent-1'
    }
    environment {
        COURSE = 'jenkins'
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                     echo "Building..."
                     env
                    """
                }
            }
        }
        stage('Test ') {
            steps {
                script {
                echo "Testing..."
                }
            }
        }
        stage('Deploy') {
            steps {
               script {
                echo "Deploying..."
                }
            }
        }
    }
    post {
        always{
            echo 'I will always say hello again!'
            deleteDir()
        }
        success {
            echo 'Hello Successs'
        }
    }
}
