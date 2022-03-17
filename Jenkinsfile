pipeline {
    parameters {
  string defaultValue: 'main', name: 'Branch'
  string defaultValue: '10', name: 'Int1'
  string defaultValue: '20', name: 'Int12'
}
   
    agent any
    stages {
        
       
        stage('Build') {
            steps {
                bat 'echo %Branch%' 
                  }
        }
        stage('Execute steps'){
            when {
                Int1 '10'
            }
            steps{
                echo 'Number is 10'
                
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
