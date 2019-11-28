node {
       def app
     
       stage('Clone repository') {
               checkout scm
       }
     
       stage('Build image'){
               app = docker.build('haseemsaeed1/example-app')
       }
   
       stage('Push iamge') {
               docker.withRegistry('https://registry.hub.docker.com', 'docker-hub-credentials') {
                      app.push('latest')
               }
}
}
