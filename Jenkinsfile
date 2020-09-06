node{
    checkout scm

    docker.withRegistry('https://registry.hub.docker.com','dockerhuba15'){

        def customImage = docker.build("179653/docker-jenkins-integration")

        customImage.push()
    }

}