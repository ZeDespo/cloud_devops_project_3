pipeline {
    agent any
    stages {
        stage('Upload to AWS') {
            steps {
                sh 'echo "Hello World"'
                sh '''echo "Multiline shell steps work too"
                      ls -lah
                   '''
                withAWS(region:'us-west-2', credentials:'aws-static') {
                    s3Upload(file:'index.html', bucket:'udacity-cloud-devops-project-3', path:'index.html')
                }
            }        
        }        
    }
}
