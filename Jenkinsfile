pipeline{
    agent any
    tools {
  maven 'Maven'
}
stages{
        stage("Maven Build"){
            when{
                branch 'develop'
            }

        }
     options {
      buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '', daysToKeepStr: '1', numToKeepStr: '5')
}

    }

              steps{
                  "mvn clean package"
              }
            }
            stage("Sonar Analysis"){
                when{
                    branch 'uat'
                }
                steps{
                    echo "sonar scanning"
                }
            }
     }
    

}