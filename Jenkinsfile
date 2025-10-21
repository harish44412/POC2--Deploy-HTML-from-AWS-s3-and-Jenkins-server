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
                withAWS(region: 'eu-north-1'
		)withCredentials([aws(accessKeyVariable: 'AWS_ACCESS_KEY_ID', credentialsId: 'my-aws-credentials', secretKeyVariable: 'AWS_SECRET_ACCESS_KEY')]) {
    // some block
} {
                    s3Upload(
                        bucket: 'htmldeploypoc1',
                        file: 'index.html',
                        acl: 'PublicRead'
                    )
                }
            }
        }
    }
}

