pipeline{

  agent any
  parameters{
    booleanParam(
      defaultValue: false,
      description: 'Skip Tests?',
      name: 'skipTests'
    )
  }
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
        when {
          expression{
            params.skipTests==false
          }
        }
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
