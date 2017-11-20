//this is the first example for pipeline as code
pipeline {
    agent any
    stages{
        stage('Build'){
            steps{
                sh 'mvn clean package'
            }
            post{
                success{
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts:'**/target/*.war'
                }
            }
        }
    }
}