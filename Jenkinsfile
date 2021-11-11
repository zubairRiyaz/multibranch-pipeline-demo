pipeline {
  
  agent any
  
    stages {
  
        stage('build') {
    
             steps {
                 echo 'builing main again'
                 echo 'builing newbranch1'
                 echo 'builing newbranch2'
             }
        }
    
        stage('test') {
    
             steps {
                 echo 'testing shell'
                 sh '/test/shell.sh'
             }
        }
    
  
        stage('deploy') {
    
             steps {
                 echo 'deploying main'
             }
        }
    }
}
