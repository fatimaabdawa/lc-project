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
                    sh "ansible-playbook ansible/build.yml -i ansible/inventory/host.yml -e ansible_become_password=123"
                }
            }
            }
            
         }
         
         }
