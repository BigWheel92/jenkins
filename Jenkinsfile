pipeline{

  agent any
  stages{

    stage("build"){
        when {
          changeRequest()
        }
      steps{
       echo 'executing yarn'
       nodejs('nodejs-19.3.0'){
        sh 'yarn install'
       }
      }
    }

    stage("test"){
      when {
          changeRequest()
        }
     steps{
      echo 'testing the application'
      }
    }

    stage("deploy"){
      when {
          changeRequest()
        }
     steps{
      echo 'deploying the application'
      }
    }

  }

}
