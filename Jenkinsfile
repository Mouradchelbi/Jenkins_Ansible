pipeline {
    agent any
    stages {
            stage ("SCM checkout") {
             steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Mouradchelbi/Jenkins_Ansible.git']])
                
                 }
        }
              stage('Ansible') {
               sh 'ansible-playbook -i inventory.ini playbook.yaml'
                   }
        
 }
}
