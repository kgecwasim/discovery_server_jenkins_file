pipeline{
    agent any
    stages{
        stage('Checkout'){
            steps{
                git(url:'https://github.com/kgecwasim/discovery_server.git')
            }
        }
        stage('build'){
            steps{
                echo 'fake build 1'
            }
        }
        stage('Deploy in docker'){
            steps{
               bat "docker container run -p 8764:8762 -d wmpoc/discovery_server:0.0.1.SNAPSHOT"
               //echo 'fake build'
            }
        }
    }
}
