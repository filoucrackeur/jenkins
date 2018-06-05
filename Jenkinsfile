pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                echo "Build...."
                parallel {
                       stage('Assets generation') { 
                           
                       }
                       stage('Installation composer') { 
                           
                       }
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
