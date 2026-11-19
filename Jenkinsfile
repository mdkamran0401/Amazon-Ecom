pipeline {
  agent any

  stages {
   
   stage('clone project') {
      steps {
           git branch:'master' , url:'https://github.com/PraveenKuberABC/Amazon-Ecom.git'
       }
   }

   stage('clean') {
      steps {
           sh 'mvn clean'
       }
   }

   stage('compile') {
      steps {
           sh 'mvn compile'
       }
   }

   stage('test') {
      steps {
           sh 'mvn test'
       }
   }

   stage('build') {
      steps {
           sh 'mvn clean install'
       }
   }
     stage('Deploy') {
    steps {
        sh 'cp Amazon/Amazon-Web/target/*.war /home/kamra/apachetomcat/apache-tomcat-9.0.123/webapps/Amazon.war'
         }
     }
  }
}
