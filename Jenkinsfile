pipeline {

    agent {
        node {
            label 'lynix-slave'
        }
    }


    stages {
        
        stage('Cleanup Workspace') {
            steps {
                cleanWs()
                sh """
                echo "Cleaned Up Workspace For Project"
                """
            }
        }

        stage('Code Checkout') {
            steps {
                checkout([
                    $class: 'GitSCM', 
                    branches: [[name: '*/main']], 
                    userRemoteConfigs: [[url: 'https://github.com/zubairRiyaz/multibranch-pipeline-demo.git']]
                ])
            }
        }


        stage('Code Analysis') {
            steps {
                sh """
                echo "Running Code Analysis"
                """
            }
        }

        stage('Build Deploy Code') {
            when {
                  Not {
                       branch 'master'
                  }
            }           
            steps {
                  sh """
                  echo "Building Artifact"
                  """

                  sh """
                  echo "Deploying Code"
                  """
            }
        }
        
        stage('Testing') {
            when {
                branch 'multibranch-sample1'
            } 
            steps {
                sh """
                echo "Running Unit Tests"
                """
            }
        }

    }   
}
