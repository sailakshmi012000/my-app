@Library("sailibs") _
pipeline{
    agent any
    stages{
        stage("git-checkout"){
            steps{
                 git credentialsId: 'github-creds', url: 'https://github.com/sailakshmi012000/my-app'
            }
        }   
         stage(maven){
             steps{
             sh 'mvn package'
             }   
         }
            stage(tomcat){
                steps{
                    //dummy edit
                    tomcatdeploy("tomcat-dev","ec2-user","172.31.88.211")
                }
            }
        }
    }
