pipeline {
  
    agent any
  
    stages {
  
        stage('build') {
    
             steps {
                 echo 'builing sample2'
                 checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/zubairRiyaz/multibranch-pipeline-demo.git']]])
             }
        }
    
        stage('test') {
    
             steps {
                 echo 'testing'
             }
        }
    
  
        stage('deploy') {
    
             steps {
                 echo 'deploying'
             }
        }
    }
}
