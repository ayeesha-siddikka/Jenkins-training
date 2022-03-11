pipeline{
    agent any
    environment{
        SECRET_TEXT = credentials("mysecret")
    }
        

    stages{
        stage("userpass"){

            environment{
                USER_PASS = credentials("userpass")
            }
            steps {
               sh 'echo "username: $USER_PASS_USR"'
               sh 'echo "password: $USER_PASS_PWD"'
               sh 'echo "username_password: $USER_PASS"'
            }
            
        }
        stage("secret"){
            steps{
                sh 'echo "mysecret: $SECRET_TEXT"'
            }
        }
         stage("all"){
            steps{
                sh "printenv"
            }
        }
    }

   
}