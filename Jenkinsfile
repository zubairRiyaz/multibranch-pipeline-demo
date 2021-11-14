pipeline {
  
    agent any
    tools {
        maven 'Maven'
    }
    stages {
  
        stage('build') {
    
            steps {
                echo 'building sample1'
                sh "mvn install"
              
            }
        }
  
        stage('test') {
    
            steps {
                echo 'testing the application'
            }
        }
  
        stage('deploy') {
    
            steps {
                echo 'deploying the application'
            }
        }
    }
}
