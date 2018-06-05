pipeline {
    agent any 
    stages {
        stage('Build') { 
            parallel {
                   stage('Assets generation') { 
                       steps {
                        echo "test...."
                       }
                   }
                   stage('Installation composer') { 
                       steps {
                        echo "test...."
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
