pipeline {
    agent any
    stages {
      stage('Upload to AWS') {
        steps {
          withAWS(region:'us-east-2',credentials:'aws-key') {
            s3Upload( file:'index.html', bucket:'jericjenkinsp4')

          }
        }
      }
    }
}

