def gv
pipeline{
    agent any
    stages{
        stage("init"){
            steps{
                script{
                    gv = load"script.groovy"
                }
            }
        }
        stage("build"){
          
            steps{
                gv.build()
            }
        }
        stage("test"){
            steps{
                script{
                    gv.testApp()
                }
            }
        }
        stage("deploy"){
            steps{
               gv.deployApp() 
            }
        }
    }
}
