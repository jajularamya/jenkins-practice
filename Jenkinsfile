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
    
}