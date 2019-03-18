pipeline {
 agent {
  label 'master'
 }
 stages {
  stage('build') {
   steps {
    sshagent(credentials: ['ssh_devops']) {
     sh 'ssh -o StrictHostKeyChecking=no -l ec2-user 172.31.46.182 uname -a'
    }
   }
  }
 }
}
