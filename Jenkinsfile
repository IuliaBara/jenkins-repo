pipeline {
    parameters {
  string defaultValue: 'main', name: 'Branch'
}
   
    agent any
    stages {
        
       
        stage('Build') {
            steps {
                bat 'echo %Branch%' 
                  }
        }
        stage('Execute bat'){
            steps{
                bat 'ls -1'
                bat 'chmod + x test.bat'
                bat './test.bat'
                
            }
        }
        stage ('Deploy'){
            steps {
                echo "Deploying stage"
            }
        }
        stage('Clean Workspace'){
            steps{
                cleanWs()
            }
        }
    }
}
