pipeline{
    agent any
    stages{
        stage("Deploy"){
            steps{
                ansiblePlaybook credentialsId: '52.139.173.104', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/test.yml'
            }
        }
    }
    
    
}


