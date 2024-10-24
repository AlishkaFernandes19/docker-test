pipeline{
    agent any
    stages{
         stage('Clean Workspace') {
            steps {
                script {
                    echo 'Cleaning workspace...'
                    bat 'if exist Jenkins-pipeline rd /s /q Jenkins-pipeline'
                }
            }
        }
    stage("cloning"){
        steps{
            script{
                 echo "cloning"
                 bat 'git clone "https://github.com/AlishkaFernandes19/docker-test.git"'
            }
        }
    
    }

   stage("build"){
        steps{
            script{
                 echo "building"
                bat 'docker build -t image:latest .'
            }
        }
    
    }

    stage("run docker container"){
        steps{
            script{
                 echo "building"
                bat 'docker run -d --name testcontainer -p 5000:5000 image:latest'
            }
        }
    
    }
}
}
