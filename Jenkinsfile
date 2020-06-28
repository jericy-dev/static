pipeline {
     agent any
     stages {
         stage('Tidy'){
            steps {
                sh 'check html file'
                sh 'tidy -q -e *.html'
            }
        }
               
         stage('Upload to AWS') {
             steps {
                withAWS(credentials: 'AKIATYYD46GTKV4M7JHI', region: 'us-east-2')
                 sh 'echo "Hello World"'
                 s3Upload acl: 'Public', bucket: 'project4jenkins', file: 'index.html' 
                 sh '''
                     echo "Multiline shell steps works too"
                     ls -lah
                 '''
             
             }
         }
     }
 }
© 2020 GitHub, Inc.
