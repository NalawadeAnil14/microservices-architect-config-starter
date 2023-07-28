pipeline {
  agent { label 'NODE2' }
  stages {
    stage('UI_Deploy')
    {
      steps {
        script {
      //    def workspace = WORKSPACE  
          sh 'echo ${env.WORKSPACE}'     
        }
      }   
    }
  }
}
