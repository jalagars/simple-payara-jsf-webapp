pipeline {
   agent any
   tools {
      maven "Maven 3.6.3"
      jdk "default"
   }
   environment {
      gitrepo = "https://github.com/jalagars/simple-payara-jsf-webapp.git"
      //added comment
      stages {
         stage('Build') {
            steps {
               // Get some code from a GitHub repository
               git "${env.gitrepo}"

               // Run Maven on a Unix agent.
               sh "mvn -Dmaven.test.failure.ignore=true clean package"

               // To run Maven on a Windows agent, use
               // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }
         }
      }
   }
}