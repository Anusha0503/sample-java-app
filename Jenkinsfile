node {

     stage('checkout'){
       git branch: 'main', credentialsId: 'anusha0503git', url: 'https://github.com/Anusha0503/sample-java-app.git'
     } 
     stage('build'){
      sh " echo ' build is running' " 
     }
     stage('deploy'){
       sh " echo 'deploy done' "
     }
}
