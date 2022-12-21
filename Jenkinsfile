pipeline{

  agent any
  stages{

    stage("build"){
      steps{
       echo 'executing yarn'
       nodejs('nodejs-19.3.0'){
        sh 'yarn install'
       }
      }
    }

    stage("test"){
     steps{
      echo 'testing the application'
      }
    }

    stage("deploy"){
     steps{
      echo 'deploying the application'
      }
    }

  }

}
