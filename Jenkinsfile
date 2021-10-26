pipeline {
   agent any
   tools {
      nodejs 'npm'
   }
   stages {
        stage('Build') { 
           steps { 
               awsCodeBuild awsAccessKey: 'AKIASFN3UMEOWJJ6GYVF', awsSecretKey: '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', credentialsType: 'keys', downloadArtifacts: 'false', projectName: ' Simple-React-Project', region: 'us-east-1', sourceControlType: 'project'
           } 
           steps {              
                sh 'npm install' 
            }
        }
      
    }
}
