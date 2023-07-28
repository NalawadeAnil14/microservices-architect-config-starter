pipeline {
  agent { label 'NODE2' }
  stages {
    stage('UI_Deploy')
    {
      steps {
        script {
           sh 'docker built -t ui-image ./ui-web-app-reactjs' 
           sh 'docker images'  
        }
      }   
    }
  }
}
