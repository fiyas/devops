pipeline {
 agent {
  label 'master'
 }
 stages {
  stage('build') {
   steps {
    sshagent(credentials: ['ssh']) {
     sh 'ssh -o StrictHostKeyChecking=no -l ec2-user uname -a'
    }
   }
  }
 }
}
