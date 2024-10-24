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
            }
        }
    }
}
