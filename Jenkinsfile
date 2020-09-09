/*
pipleline{
    agent none
    stages{
        stage('Maven Install'){
            agent any
            steps{
                sh 'mvn -f pom.xml clean install'
            }
        }
        stage('Docker Build'){
            agent any
            steps{
                sh 'docker build -t 179653/docker-jenkins-integration .'
            }
        }
        stage('Docker Push'){
            agent any
            steps{
                withDockerRegistry([ credentialsId: "dockerhub", url: ""]){
                    sh 'docker push 179653/docker-jenkins-integration'
                }
            }
        }
    }
}

pipeline {
     agent any
     stages {
          stage("Compile") {
               steps {
                    sh "./mvnw compile"
               }
          }

     }
}
*/

pipeline {
     agent any
     stages{
        stage('Maven Install'){
                      agent any
                      steps{
                          bat 'mvn -f pom.xml clean install'
                      }
                  }
     }
}


























