node {

     stage('checkout'){
            git branch: 'main', credentialsId: 'gitcredentials', url: 'https://github.com/Anusha0503/sample-java-app.git'
     } 
     stage('build'){
            withMaven(globalMavenSettingsConfig: '', jdk: 'java', maven: 'maven', mavenSettingsConfig: '', traceability: true) {
            sh " mvn clean package" 
             }
     }
     stage('deploy'){
       sh " sudo nohup java -jar target/*.jar > nohup.out 2>&1 &"
     }
}
