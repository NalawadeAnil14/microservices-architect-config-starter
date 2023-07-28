pipeline {
  agent { label 'NODE2' }
  stages {
    stage('UI_Deploy')
    {
      steps {
        script {
          def workspace = env.WORKSPACE  
          sh 'echo $workspace'     
        }
      }   
    }
  }
}
