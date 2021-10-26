pipeline{
    agent any
    tools {
  maven 'Maven'
}
stages{
        stage("Maven Build"){
            when{
                branch "develop"
            }
              steps{
                  "mvn cleanpackage"
              }
            }
            stage("Sonar Analysis"){
                when{
                    branch "uat"
                }
                steps{
                    echo "sonar scanning"
                }
            }
     }
    
}