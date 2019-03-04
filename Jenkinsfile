node {

    stage('Clone Repository')
    {
        checkout scm
    }

    stage('Show me the files') {

        sh "ls -l"	
       
    }
     stage('Build docker image') {

     app= docker.build("DOCKER_TEST:0.1")
       
    }
    stage('Docker login to hub and push the image') {

        // This step should not normally be used in your script. Consult the inline help for details.
        withDockerRegistry(toolName: 'Docker', url: 'docker.io') {
            
              app.push("latest")
            // some block
        }
  
}
    }
    
      stage('Apply changes to the environment') {

        sh "ls -l"	
        sh "echo run application"
       
    }
}
