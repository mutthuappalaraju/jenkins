pipeline {
    
    agent {
        node {
            label 'AGENT-1'
        
        }
    }
    // options {
    //     // Timeout counter starts AFTER agent is allocated
    //     timeout(time: 1, unit: 'HOURS')
    // }

    environment { 
       GREETING = 'hello jenkins'
    }

    
    
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                sh """
                   echo 'heloo shell script'
                   env
                """   
                
            }
        }
    }
    post { 
        always { 
            echo 'I will always say Hello again!'
        }
        failure { 
            echo 'when indicate job failure'
        }
        success { 
            echo 'when job success'
        }
    }
}


