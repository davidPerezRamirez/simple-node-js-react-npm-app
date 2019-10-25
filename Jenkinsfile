pipeline {
    agent {
        docker {
            image 'node:6-alpine' 
            args '-p 3000:3003' 
        }
    }
    triggers {
      pollSCM '*/1 * * * *'
    }
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
