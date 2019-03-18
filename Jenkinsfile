pipeline {
 agent {
  label 'master'
 }
 stages {
  stage('build') {
   steps {
    sshagent(credentials: ['ssh']) {
     sh 'ssh -p 22 -o StrictHostKeyChecking=no -l ec2-user 13.58.251.0 uname -a'
    }
   }
  }
 }
}
