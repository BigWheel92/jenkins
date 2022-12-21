pipeline{

  agent any
  stages{

    stage("build"){
        when {
          getGitChanges()==true
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
          getGitChanges()==true
        }
     steps{
      echo 'testing the application'
      }
    }

    stage("deploy"){
      when {
          getGitChanges()==true
        }
     steps{
      echo 'deploying the application'
      }
    }

  }

}
