node {

     stage('checkout'){
            git branch: 'main', credentialsId: 'anusha0503git', url: 'https://github.com/Anusha0503/sample-java-app.git'
     } 
     stage('build'){
            withMaven(globalMavenSettingsConfig: '', jdk: 'java11', maven: 'maven', mavenSettingsConfig: '', traceability: true) {
            sh " mvn clean package" 
             }
     }
     stage('deploy'){
       sh " nohup java -jar target/*.jar > nohup.out 2>&1 &"
     }
}
