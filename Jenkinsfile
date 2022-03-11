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
                node
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