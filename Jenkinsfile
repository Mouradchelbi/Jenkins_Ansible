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
                ansiblePlaybook credentialsId: 'Ansibleprivatekey_apacheVM', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dev.inv', playbook: 'roles/apache.yaml'
            }    
        }   
       }
}
