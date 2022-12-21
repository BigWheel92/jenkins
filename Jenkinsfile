pipeline{

  agent any
  stages{

    stage("build"){
        when {
          expression{
          changeRequest()==true
          }
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
          expression{
          changeRequest()==true
          }
        }
     steps{
      echo 'testing the application'
      }
    }

    stage("deploy"){
        when {
          expression{
          changeRequest()==true
          }
        }
     steps{
      echo 'deploying the application'
      }
    }

  }

}
