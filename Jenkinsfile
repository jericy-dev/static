 
pipeline{
        agent any
        stages {
           
           
            stage('Upload to AWS') {
                steps {
                    
                        withAWS(region:'us-east-2', credentials:'aws-static',role: 'arn:aws:iam::259316838822:user/jericp4'){
                        s3Upload(file:'index.html', bucket:'jericjenkinsp4', path:'')
                                                
                }
            }
        }
    }
}
