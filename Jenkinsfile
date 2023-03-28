pipeline{
agent any
stages{
    stage("Git checkout"){
        steps{
            git credentialsId: 'html_home', url: 'https://github.com/B-Apoorva/Project1.git'
        }
    }
    stage("Maven Build"){
        steps{
        sh "mvn compile"
        sh "mvn test"
        sh "mvn clean package"
        sh "mv target/*.war target/myweb.war"
        }
    }
   
    }
}
