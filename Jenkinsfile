pipeline{
    agent any
    environment{
        SECRET_TEXT = credentials('suprise')
    }
    stages{
        stage("build"){
            environment{
                USER_PASS = credentials('userpassword')
                   
            }
            steps{
                echo "testing the text"
                sh 'echo "username: $USER_PASS_USR"'
               sh 'echo "password: $USER_PASS_PSW"'
               sh 'echo "username_password: $USER_PASS"'
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
