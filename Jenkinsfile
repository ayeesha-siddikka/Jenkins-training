pipeline{
    agent any
    stages{
        stage("build"){
            agent {
                docker {
                    image 'maven:3.8.1-adoptopenjdk-11'
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
            agent { docker 'openjdk:8-jre' } 
            steps {
                echo 'Hello, JDK'
                sh 'java -version'
            }
        }

    }
}