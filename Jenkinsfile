pipeline {
     agent any
     stages {
         stage('Upload to AWS.') {
             steps {
                 sh 'echo "Hello World!"'
                 withAWS(region:'us-west-2',credentials:'aws-static') {
                  sh 'echo "Uploading content with AWS creds"'
                      s3Upload(file:'index.html', bucket:'udacitycicd-project3')
                  }
             }
         }  
     }
}
