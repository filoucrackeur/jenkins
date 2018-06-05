pipeline {
    agent any 
    environment {
        TYPO3_CONTEXT = 'Development'
    }
    parameters {
        string(name: 'TYPO3_CONTEXT', defaultValue: 'Development/Qua', description: 'Environnement TYPO3')
    }
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
                echo ${env.GIT_BRANCH}
                echo "test...."
            }
        }
        stage('Deploy') { 
            when {
                branch 'origin/master'
                environment name: 'TYPO3_CONTEXT', value: 'Production'
            }
            steps {
                echo 'Deploying prod'
            }
        }
    }
}

