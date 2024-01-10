pipeline {
    agent any
    
    stages {
        
        stage("build and test"){
            steps{
                sh "docker build -t node-app-test-new ."
                echo 'code build bhi ho gaya'
            }
        }

        stage("deploy"){
            steps{
                sh "docker run -p 8081:8081 node-app-test-new"
                echo 'deployment ho gayi'
            }
        }
    }
}
