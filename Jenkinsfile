pipeline{
    agent any
    stages{
        stage("build"){
            steps{
                echo("build jenkins file")
            }
        
        }
        
        stage("test"){
            when {
                expression{
                    BRANCH_NAME == "develop"
                }
            }
            node {
                steps{
                    echo("testing")
                }
            }
            
        }

    }
}