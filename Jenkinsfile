pipeline {
   agent any
   tools {
      nodejs "nodejs 16.11.1"
   }
   stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
    }
}
