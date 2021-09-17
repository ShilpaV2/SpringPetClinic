pipeline{
    agent any
    tools {maven 'M3'}
    
    stages{
    
    stage('checkout') 
    {
        steps{
            git branch: 'main',
            credentialsId: '324ad7ae-8615-40f7-8d71-2b4b5735d0c4',
            url: 'https://github.com/ShilpaV2/SpringPetClinic.git'
            echo 'checkout SCM done'
}
}
stage('Build')
{ 
    steps{
       sh 'mvn compile'
}
}

stage ('Test')
{
    steps{
        sh 'mvn test'
    }
}
stage('package')
{
    steps{
        sh 'mvn package'
    }
}
stage('Deploy')
{
    steps{
        sh 'java -jar /*/target/*.jar'
    }
}
}
}
