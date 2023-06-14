pipeline {
    agent any
    stages {
        stage ("SCM checkout") {
            steps {
               checkout scmGit(branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/Mouradchelbi/Jenkins_Ansible.git']])
                
                 }
        }
<<<<<<< HEAD
        stage('Ansible') {
        sh 'ansible-playbook -i inventory.ini Playbook.yaml'
                   }
                   }
                   }
=======
        stage(" execute Ansible") {
           steps {
                ansiblePlaybook credentialsId: 'Ansibleprivatekey_apacheVM', disableHostKeyChecking: true, installation: 'Ansible', inventory: 'dev.inv', playbook: 'roles/apache.yaml'
            }    
        }   
       }
}
>>>>>>> 6a8ef5ec266667fdb8540dec41700d39851f41fe
