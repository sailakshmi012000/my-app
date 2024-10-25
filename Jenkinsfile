@Library("sailibs") _
pipeline{
    agent{
        label "linux"
    }
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
                    tomcatdeploy("tomcat-dev","ec2-user","172.31.88.211")
                }
            }
        }
    }
