 
pipeline{
        agent any
        stages {
           
           
            stage('Upload to AWS') {
                steps {
                    
                        withAWS(region:'us-east-2', credentials:'aws-static1'){
                        s3Upload(file:'index.html', bucket:'jericjenkinsp4', path:'')
                                                
                }
            }
        }
    }
}
