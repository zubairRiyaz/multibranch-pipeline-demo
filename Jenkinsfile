pipeline {
  
  agent any
  
    stages {
  
        stage('build') {
    
             steps {
                 git branch: 'multibranch-sample1', url: 'https://github.com/zubairRiyaz/multibranch-pipeline-demo.git'
                 echo 'builing main again'
                 echo 'builing newbranch1'
             }
        }
    
        stage('test') {
    
             steps {
                 echo 'testing shell'
                 sh "chmod +x -R ${env.WORKSPACE}"
                 sh './test/shell.sh'
             }
        }
    
  
        stage('deploy') {
    
             steps {
                 echo 'deploying main'
             }
        }
    }
}
