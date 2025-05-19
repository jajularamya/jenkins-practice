pipeline {
    agent { label 'agent-1' }
    environment { 
        PROJECT = 'EXPENSE'
        COMPONENT = 'BACKEND' 
        DEPLOY_TO = "production"
    }
    options {
        disableConcurrentBuilds()
        timeout(time: 30, unit: 'MINUTES')
    }
    parameters{
        string(name: 'PERSON', defaultValue: 'Mr Jenkins', description: 'Who should I say hello to?')
        text(name: 'BIOGRAPHY', defaultValue: '', description: 'Enter some information about the person')
        booleanParam(name: 'TOGGLE', defaultValue: true, description: 'Toggle this value')
        choice(name: 'CHOICE', choices: ['One', 'Two', 'Three'], description: 'Pick something')
        password(name: 'PASSWORD', defaultValue: 'SECRET', description: 'Enter a password')
    }
    stages {
        stage('build') {
            steps {
                script{
                 sh """
                    echo "hello this is build"
                    echo "project: $PROJECT"
                    sleep 15
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