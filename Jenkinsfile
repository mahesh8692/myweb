pipeline{
    agent any
    tools {
     maven 'maven3'
    }
    stages{
        stage("Git Checkout"){
            steps{
                git credentialsId: 'maheshgit', url: 'https://github.com/mahesh8692/myweb'
            }
        }
        stage("Maven Build"){
            steps{
                script{
                    if(isUnix()){
                        sh 'mvn clean package'
                    }
                }
            }
        }
    }
}
