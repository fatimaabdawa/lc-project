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

      







            
         }
         
         }
