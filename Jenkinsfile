pipeline {
    agent any
    stages {
        stage('Clone Git Repository') {
            steps {
                git branch: 'main', url: 'https://github.com/gujjar-aditya/jenkins-ansible.git'
            }
        }

        stage('Run Ansible Playbook') {
            steps {
                sh 'ansible-playbook -i inventory.ini install_apache.yml'
            }
        }
    }

}

