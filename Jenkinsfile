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
  }
}
