pipeline{
    agent any
    stages{
        stage("build"){
            agent{
                docker{
                    image 'node'
                }
            }
            steps {
                echo " building the text"
                sh 'node --version'
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
            agent{
                docker{
                    image 'python'
                    
                }
            }
            steps{
                echo"deploying the text"
                sh 'python --version'
            }
        }
    }
}