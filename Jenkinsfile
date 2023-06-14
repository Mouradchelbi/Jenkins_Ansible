pipeline {
    agent any
    stages {
            stage ("SCM checkout") {
             steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Mouradchelbi/Jenkins_Ansible.git']])
                
                 }
               }
              
               stage(" execute Ansible") {
               steps {
                ansiblePlaybook credentialsId: 'private-key', disableHostKeyChecking: true, installation: 'inventory.ini', inventory: 'dev.inv', playbook: 'apache.yml'
            }    
   }    
}
