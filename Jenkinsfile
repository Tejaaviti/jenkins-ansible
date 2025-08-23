pipeline {
    agent any

    stages {
        stage('cloning github repo') {
            steps {
                git 'https://github.com/Tejaaviti/jenkins-ansible'
                echo 'Clonning....'
            }
        }
        stage('Run Ansible Playbook'){
            steps{
                ansiblePlaybook credentialsId: 'ansible-ssh', disableHostKeyChecking: true, installation: 'ansible2', inventory: 'inventory.ini', playbook: 'install_apache.yml', vaultTmpPath: ''
            }
        }
    }
}
