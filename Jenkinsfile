pipeline {
    agent { label 'agent-1' }
    stages {
        stage('build') {
            steps {
                script{
                 sh """
                    echo "hello this is build"
                 """
                }
                
            }
        }
        stage('test') {
            steps {
                script{
                 sh """
                    echo "hello this is test"
                 """
                }
            }
        }
        stage('deploy') {
            steps {
                script{
                 sh """
                    echo "hello this is deploy"
                 """
                }
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'I will run when pipeline is failed'
        }
        success { 
            echo 'I will run when pipeline is success'
        }
    }
    
}