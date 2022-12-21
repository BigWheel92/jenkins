pipeline{
 
  agent any
  stages{

    stage("build"){
      steps{
        echo 'executing yarn'
        nodejs('nodejs-1.3.0'){
        sh 'yarn'
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
