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
       deploy adapters: [tomcat9(credentialsId: 'tomcat', path: '', url: 'http://54.226.206.216:8080/')], contextPath: null, war: '**/*.war'     }
}
