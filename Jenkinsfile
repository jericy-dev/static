pipeline {
    agent any
    stages {
      stage('Upload to AWS') {
        steps {
          withAWS(region:'us-east-2',credentials:'AKIATYYD46GTKV4M7JHI') {
            s3Upload(pathStyleAccessEnabled:true, payloadSigningEnabled: true, file:'index.html', bucket:'jericjenkinsp4')

          }
        }
      }
    }
}

