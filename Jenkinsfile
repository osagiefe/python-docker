pipeline{
    agent any
    stages{
        stage("Github checkout"){
            steps {
                script {
 
                    git branch: 'main', url: 'https://github.com/osagiefe/python-docker.git' 
                }
            }

        }
               stage("build your docker image"){
            steps{
                script{
                    sh 'printenv'
                    sh 'git version'
                    sh 'docker build . -t osagiefe/imag2.0' 
               
            
                }
            }
        }
               stage("push docker image to dockerhub"){
            steps{
                script {
                    withCredentials([string(credentialsId: 'DockerID', variable: 'DockerID')]) {
                        sh 'docker login -u osagiefe -p ${DockerID}'
                   }
                   sh 'docker push osagiefe/imag2.0:latest'
            }
            }
        }
    }
}
