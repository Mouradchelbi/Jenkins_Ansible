pipeline {
    agent any
    stages {
            stage ("SCM checkout") {
             steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Mouradchelbi/Jenkins_Ansible.git']])
                
                     }
              }
         
       ansiblePlaybook becomeUser: null, credentialsId: 'ssh-agent', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/var/lib/jenkins/workspace/Jenkins_Ansible/inventory.ini', playbook: '/var/lib/jenkins/workspace/Jenkins_Ansible/roles/playbook.yaml
      }
}
