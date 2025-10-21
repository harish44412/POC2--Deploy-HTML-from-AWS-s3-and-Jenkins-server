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
                withAWS(region: 'eu-north-1', credentials: 'AKIARBFZBHNQH3BSGRRD') {
                    s3Upload(
                        bucket: 'htmldeploypoc1',
                        path: '',
                        file: 'index.html',
                        acl: 'PublicRead'
                    )
                }
            }
        }
    }
}

