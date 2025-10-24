-Create folder in local
-Add index.html and contents
-Add jenkinsfile

-Start git = #git init
-#git add
-#git commit -m "add your message"
-#git branch -M master/main
-#git remote add origin 'repolink'
-#git push -u origin master/main

-Create s3 with static enabled and acl disabled,iam with s3fullaccess policy, EC2 and install jdk 17 & Jenkins in root account
-download zip file of awscli and unzip and install awscli
-configure aws account
-setup jenkins
-add aws credentials and s3 plugin
-add iam accesskey and secret key and unique id which to be used in jenkinsfile

Create new pipeline
configure git
configure webhook

Buil Now, i have not disabled ACL in s3 bucket so the jenkin build will fail
