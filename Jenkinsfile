pipeline {
 agent {
  label 'master'
 }
 stages {
  stage('info') {
   steps {
    sshagent(credentials: ['ssh']) {
     sh 'ssh -p 22 -o StrictHostKeyChecking=no -l ec2-user 13.58.251.0 uname -a'
    } 
   }
  }
  stage('aws') {
   steps {
    sshagent(credentials: ['ssh']) {
    withCredentials([[$class: 'AmazonWebServicesCredentialsBinding', credentialsId: 'JenkinsAWSKeys']]) {
    sh 'aws s3api list-buckets --query "Buckets[].Name"'
}   
}
 }
 }
}
}
