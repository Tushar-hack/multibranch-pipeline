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
                echo "This will build the app...."
                script{
                    gv.buildApp()
                }
            }
        }
        stage("test"){
            steps{
                echo "This will test the code...."
                script{
                    gv.testApp()
                }
            }
        }
        stage("deploy"){
            steps{
                echo "This will deploy the app...."
                script{
                     gv.deployApp() 
                }
            }
        }
    }
}
