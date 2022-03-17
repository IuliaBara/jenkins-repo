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
        stage('Test'){
            steps{
                echo "Testing stage"
            }
        }
        stage ('Deploy'){
            steps {
                echo "Deploying stage"
            }
        }
    }
}
