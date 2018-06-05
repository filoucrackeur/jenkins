pipeline {
    agent any 
    stages {
        stage('Build') { 
            parallel {
                   stage('Assets generation') { 
                        echo "test...."
                   }
                   stage('Installation composer') { 
                        echo "test...."
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
