pipeline{
    agent any
    stages{
        stage("Github checkout"){
            steps{
                script{
                    sh 'printenv'
                    echo "github checkout"
                }
            }
        }
               stage("build your docker image"){
            steps{
                script{
                    sh 'printenv'
                    echo "build docker image"
                }
            }
        }
               stage("push docker image to dockerhub"){
            steps{
                script{
                    sh 'printenv'
                    echo "push to dockerhub"
                }
            }
        }
    }
}
