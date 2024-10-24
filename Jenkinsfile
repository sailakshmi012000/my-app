@Library("sailibs") _
pipeline{
    agent any
    
    stages{
        stage("maven-build"){
            steps{
                sh 'mvn clean package'
            }
        }
        stage("tomcat-deploy"){
            steps{
                tomcatdeploy("tomcat-dev","ec2-user","172.31.88.211")

            }
        }
    }
}
