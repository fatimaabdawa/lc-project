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

       stage('python test'){
            steps{
                script{
                    sh "python3 --version"
                }
            }
        }
        stage('Build'){
            steps{
                script{ 
                    sh "ansible-playbook Ansible/build.yml -i Ansible/inventory/host.yml"
                }
            }
            }
            
            stage('docker'){
            steps{
                script{
                    sh "python3 --version"
                }
            }
        }


  stage('docker-registry'){
            steps{
                script{
                   sh "python3 --version"
                }
            }
        }







         }
         
         }
