pipeline{
  agent {docker {image 'maven'}
  stages{
    stage('developer build'){
      steps{
        dir ('projects/org.javacream.util.library'){
          sh "mvn -Dmaven.test.failure.ignore=true clean package"
       } 
      }
    }
  }
}
