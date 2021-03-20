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
        sh 'docker login'
        sh 'docker push ankitaj86/phpmysql_app:latest'
    }
}
