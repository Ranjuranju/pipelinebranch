pipeline{
    agent any
    stages{
        stage("SCM"){
            steps{
               echo "job ran.....again and again"
            }
        }
     options {
      buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '1', numToKeepStr: '5')
}

    }
}