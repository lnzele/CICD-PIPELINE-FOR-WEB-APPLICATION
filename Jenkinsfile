def gv

pipeline{
    agent any


environment {
    TAG = '1.2'
    PORT = '80'
}




    stages{
        stage("init"){
            steps{
                script{
                    gv = load "script.groovy"
                }
                
            }
        }

        stage("Build"){
            steps{
                script{
                    gv.Build()
                }
            }
        }

        stage("Test"){
            steps{
                script{
                    gv.Test()
                    echo "Test by webhook from github"
                }
            }
        }

        stage("Deploy"){
            steps{
                script{
                    gv.Deploy()
                }
            }
        }
    }
}