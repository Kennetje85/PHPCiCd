pipeline{
    agent any
    stages{
        stage("playbook execute"){
            steps{
                ansiblePlaybook credentialsId: '52.139.173.104', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/test.yml'
            }
        }
    }
    
    
}


