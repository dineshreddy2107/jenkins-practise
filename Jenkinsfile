pipeline {
    agent {
        label 'agent-1'
    }
    environment {
        COURSE = 'jenkins'
    }
    options {
        timeout(time: 30, unit: 'MINUTES')
        disableConcurrentBuilds()
    }
    stages {
        stage('Build') {
            steps {
                script {
                    sh """
                     echo "Building..."
                     sleep 10
                     
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
