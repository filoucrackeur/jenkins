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
                                                  input message: 'Environnement à deployer ?', ok: 'Deployer', parameters: [choice(choices: ['Development/Qua', 'Development/Tma', 'Testing/Qua', 'Testing/Tma', 'Testing/Prj', 'Testing/Preprod', 'Production'], description: '', name: 'environnement')]

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
                echo "${env.GIT_BRANCH}"
                echo "test...."
            }
        }
        stage('Deploy') { 
            when {
                expression {
                    BRANCH_NAME == 'master'
                }
            }
            steps {
                echo 'Deploying prod'
            }
        }
    }
}

