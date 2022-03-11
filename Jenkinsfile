pipeline{
    agent any
    environment{
        SECRET_TEXT = credentials('suprise')
    }
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
        stage('userpass'){
            environment{
                USER_PASS = credentials('userpassword')
            }
            steps{
                sh 'echo "username: $USER_PASS_USR"'
               sh 'echo "password: $USER_PASS_PSW"'
               sh 'echo "username_password: $USER_PASS"'

            }

        }
    }
}