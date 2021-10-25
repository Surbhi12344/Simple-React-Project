pipeline {
   agent any
   tools {
      nodejs 'npm'
   }
   stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Upload to S3') { 
            steps {
                dir(''){

                  pwd(); //Log current directory

                  withAWS(region:'us-east-1',credentials:'7b5ae1e9-91c4-4f8f-b369-0d464ce9e4b1') {

                        def identity=awsIdentity();//Log AWS credentials

                        // Upload files from working directory 'dist' in your project workspace
                        s3Upload(bucket:"jenkins.deployment", workingDir:'', includePathPattern:'**/*');
                  }

               };
            }
        }
      
    }
}
