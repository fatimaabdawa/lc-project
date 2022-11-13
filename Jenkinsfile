pipeline {
    agent any
    stages {
        stage ("Pull") {
            steps{
                script{
                    checkout([$class: 'GitSCM', branches: [[name: '*/master']],
                    userRemoteConfigs:[[
                        credentialsId: 'github', url: 'https://github.com/fatimaabdawa/lc-project.git']]])
                }
            }
        }

      stage('Build'){
            steps{
                script{   
                    sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml -e ansible_become_password=123"
                }
            }
            }
            

  stage('docker'){
            steps{
                script{
                    sh "ansible-playbook Ansible/docker.yml -i Ansible/inventory/host.yml"
                }
            }
        }








         }
         
         }
