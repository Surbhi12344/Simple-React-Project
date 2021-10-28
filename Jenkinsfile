pipeline {
   agent any
   tools {
      nodejs 'npm'
   }
   stages {
        stage('Build') { 
           steps { 
               awsCodeBuild credentialsType: 'keys', downloadArtifacts: 'false', projectName: ' Simple-React-Project', region: 'us-east-1', sourceControlType: 'project'           
               sh 'npm install' 
            }
        }
      
    }
}
