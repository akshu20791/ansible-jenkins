pipeline {
    agent any
    stages{
        stage("clone the github repo"){
            steps{
                git 'https://github.com/akshu20791/ansible-jenkins/'
            }
        }
        stage("run the ansible-playbook"){
            steps{
                ansiblePlaybook credentialsId: 'ansible-ssh', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'inventory.ini', playbook: 'install_apache.yml', vaultTmpPath: ''
            }
        }
    }
}
