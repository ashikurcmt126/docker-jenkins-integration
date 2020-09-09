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
    agent none
   stages {
    stage('Maven Install') {
      agent {
       docker {
         image 'apache-maven-3.6.3'
     }
  }
  steps {
       sh 'mvn clean install'
       }
     }
   }
 }





























