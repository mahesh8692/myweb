pipeline{
    agent any
    stages{
        stage("Git Checkout"){
            steps{
                git credentialsId: 'maheshgit', url: 'https://github.com/mahesh8692/myweb'
            }
        }
        stage("Maven Build"){
            steps{
                script{
                        sh 'mvn clean package'
                }
            }
        }
    }
}
