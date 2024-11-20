pipeline {
    agent {
        label 'AGENT-1'
    }

    options {
        timeout(time: 10, unit: 'SECONDS') 
    }

    environment { 
        CC = 'clang'
    }
    
    stages {
        stage('Build') {
            steps {
                sh 'echo This is build'
                sh 'env'
                sh 'sleep 15'
            }
        }
        stage('Test') {
            steps {
                sh 'echo This is Test'
            }
        }
        stage('Deploy') {
            steps {
                sh 'echo This is Deploy'
            }
        }
        stage("print params"){
            steps{
                sh 'echo This is Deploy'
                sh 'env'
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        success { 
            echo 'I will run when pipeline is success'
        }
        failure { 
            echo 'I will run when pipeline is failure'
        }
    }
}