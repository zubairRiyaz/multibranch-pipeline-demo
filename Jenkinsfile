pipeline {
  
    agent any
    parameters {
        choice(name: 'VERSION', choices: ['1.1', '1.2', '1.3'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }
    stages {
  
        stage('build') {
    
            steps {
                echo 'building sample1'
                
              
            }
        }
  
        stage('test') {
            when {
                expression { 
                    params.executeTests == true
                }
            }  
            steps {
                echo 'testing the application'
            }
        }
  
        stage('deploy') {
    
            steps {
              echo "deploying version ${params.Version}"
            }
        }
    }
}
