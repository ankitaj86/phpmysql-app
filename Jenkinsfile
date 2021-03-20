node{

    stage('SCM Checkout')
    {
        git url: 'https://github.com/ankitaj86/phpmysql-app.git'
    }
    
    stage('Run Docker Compose File')
    {
        sh 'docker-compose build'
        sh 'docker-compose up -d'
    }
    stage('PUSH image to Docker Hub')
    { 
        
        withDockerRegistry([ credentialsId: "docker", url: "https://index.docker.io/v1/" ]) {
                                    bat "docker push ankitaj86/phpmysql_app:lates"
                                     }

    }
}
