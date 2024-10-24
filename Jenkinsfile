@Library("sailibs") _
pipeline{
    agent any

    stages{
        stage("maven build"){
            when{
                branch "develop"
            }
            steps{
                sh "mvn package"
            }
        }
        stage("deploy"){
            when{
                branch "master"
            }
            steps{
                echo "deploy to master server..."

    
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
