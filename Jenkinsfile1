pipeline {
    agent any
    stages {
        stage("bulid") {
            agent {
                docker {
                    image "python"
                    reuseNode true
                }
            }
            steps {
                echo("building python")
                sh "python --version"
                echo("build completed")
            }
        }
        stage("test"){
            steps{
                echo("testing stage")
            }
        }
        stage("deploy"){
            agent {
                docker{
                    image "python:3.9-bullseye"
                    reuseNode true
                }
            }
             steps {
                echo("deploying python")
                sh "python --version"
                echo("deployed")
            }

        }
    }
}