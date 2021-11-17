pipeline {
    agent any
    stages {
        stage('Example Build') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Example Deploy') {
            when {
                branch 'newbranch2'
                
            }
            steps {
                echo 'Deploying'
            }
        }
    }
}
