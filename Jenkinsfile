pipeline {
    agent any 
    stages {
        stage('Build') { 
                parallel {
                       stage('Assets generation') { 
                           
                       }
                       stage('Installation composer') { 
                           
                       }
                }
        }
        stage('Test') { 
            steps {
                echo "test...."
            }
        }
        stage('Deploy') { 
            steps {
                echo "deploy...."
            }
        }
    }
}
