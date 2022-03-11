pipeline{
    agent any
    stages{
        stage("build"){
            steps {
                echo " building the text"
            }
        }
        stage("test"){
            when{
                expression{
                    BRANCH_NAME == "develop"
                }
            }
            steps{
                echo "testing the text"
            }
        }
        stage("deploy"){
            steps{
                echo"deploying the text"
            }
        }
    }
}