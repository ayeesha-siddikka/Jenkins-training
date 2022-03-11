pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                echo("build jenkins file")
            }
        
        }
        
        stage("test"){
            agent {
                node any
            }
            
            when {
                expression{
                    BRANCH_NAME == "develop"
                }
            }
            steps{
                echo("testing")
            }
        }

    }
}