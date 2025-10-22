pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                echo 'Cloning repository...'
                git branch: 'master', url: 'https://github.com/harish44412/POC2--Deploy-HTML-from-AWS-s3-and-Jenkins-server.git'
            }
        }
        stage('Deploy to S3') {
            steps {
                echo 'Deploying to AWS S3...'
                withAWS(region: 'eu-north-1', credentials: 'my-aws-credentials')

} {       sh 'aws s3 sync . s3://my-simple-poc-website'
                    s3Upload(
                        bucket: 'my-simple-poc-website',
                        file: 'index.html',
                        acl: 'PublicRead'
                    )
                }
            }
        }
}


