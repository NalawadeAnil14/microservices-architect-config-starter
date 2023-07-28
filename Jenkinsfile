pipeline {
  agent { label 'NODE2' }
  stages {
    stage('UI_Deploy')
    {
      steps {
        script {
           sh 'docker build -t ui-image ./ui-web-app-reactjs' 
           sh 'docker images' 
           sh 'docker run -itd --name ui-screen -p 8080:8080 ui-image' 
           sh 'docker ps'   
        }
      }   
    }

    stage('Zuul-server')
    {

      steps {
        script {
           sh 'docker build -t zuul-image ./zuul-api-gateway'
           sh 'docker images'
           sh 'docker run -itd --name zuul-server zuul-image'
           sh 'docker ps'
        }
      }
    }

    stage('shoes')
    {

      steps {
        script {
           sh 'docker build -t shoes-image ./shoes-microservice-spring-boot'
           sh 'docker images'
           sh 'docker run -itd --name shoes-server shoes-image'
           sh 'docker ps'
        }
      }
    }

    stage('offers')
    {

      steps {
        script {
           sh 'docker build -t offer-image ./offers-microservice-spring-boot'
           sh 'docker images'
           sh 'docker run -itd --name offer-server offer-image'
           sh 'docker ps'
        }
      }
    }

  }
}
