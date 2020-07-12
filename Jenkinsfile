pipeline {
   agent any 
   tools {
        maven 'Maven4.0.0' 
    }
   
   stages {
       stage('SCM CheckOut'){
          steps {
            git 'https://github.com/debashis-1306/TestApp'
          }
          }
      stage('Compile-Package'){
         steps {
             sh "mvn -version"
             sh "mvn clean install" 
             sh "mvn package"
              }
         }
   }
   post {
      always {
         cleanWs()
      }
   }
}
