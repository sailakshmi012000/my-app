pipeline{
    agent any
    stages{
        stage("demo"){
            when{
                branch "develop"
            }
            steps{
                echo "Hai, sai"
            }    
        }
        stage("maven"){
            when{
                branch "master"
            }
            steps{
                sh 'mvn package'
            }
        }
    }
}
