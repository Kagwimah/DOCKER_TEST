node {

    stage('Clone Repository')
    {
        checkout scm
    }

    stage('Show me the files') {

        sh "ls -l"	
       
    }
     stage('Build docker image') {

        sh "docker build -t DOCKER_TEST:0.1 ."	
       
    }
    stage('Docker login to hub and push the image') {

        sh "docker login  -u "kagwima" -p "K@d506112007" "	
        sh "docker tag DOCKER_TEST:0.1 kagwima/docker_test:latest"
        sh "docker push kagwima/docker_test:latest"
       
    }
    
      stage('Apply changes to the environment') {

        sh "ls -l"	
        sh "echo run application"
       
    }
}
