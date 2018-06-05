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
                        echo "tests...."
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
            when {
                branch 'master'
                environment name: 'TYPO3_CONTEXT', value: 'Production'
            }
            when {
                branch 'qua'
                environment name: 'TYPO3_CONTEXT', value: 'Testing/Qua'
            }
            when {
                branch 'development'
                environment name: 'TYPO3_CONTEXT', value: 'Development/Qua'
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}

