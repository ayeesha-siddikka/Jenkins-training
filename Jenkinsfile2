pipeline{
    agent any
    stages{
        stage("build"){
            agent {
                docker {
                    image 'maven:3.8.1-adoptopenjdk-11'
                    reuseNode true
                }
                
            }
            steps{
                echo("build start")
                sh 'mvn --version'
                echo("build finished")
            }
        
        }
        
        stage("test"){
            when {
                expression{
                    BRANCH_NAME == "develop"
                }
            }
            steps{
                echo("testing")
            }
        }
        stage('Example Test') {
            agent { 
                docker {
                    image 'openjdk:8-jre'
                    reuseNode true
                }
            }
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
            }
        }

    }
}