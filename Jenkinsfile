node {

    stage('Clone Repository')
    {
        checkout scm
    }

    stage('Show me the files') {

        sh "ls -l"	
       
    }
     stage('Build docker image') {

     app= docker.build("docker-test:0.1")
       
    }
    stage('Docker login to hub and push the image') {

        // This step should not normally be used in your script. Consult the inline help for details.
          withDockerRegistry(credentialsId: 'b5588a7a-3945-46a6-b072-9832a91596e6' ,toolName: 'Docker', url: 'docker.io/kagwima') {
            // some block
            app.push("latest")
        }
    
}
    
      stage('Apply changes to the environment') {

        sh "ls -l"	
        sh "echo run application"
       
    }
}
