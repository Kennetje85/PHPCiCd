pipeline{
    agent any
    stages{
        stage("playbook execute"){
            steps{
                ansiblePlaybook credentialsId: 'jenkinsAnsible', disableHostKeyChecking: true, installation: 'Ansible', inventory: '/etc/ansible/hosts', playbook: '/etc/ansible/test.yml'
            }
        }
    }
}
