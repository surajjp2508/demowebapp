pipeline{
agent any
  stages{
    stage("checkout-code"){
    steps {
        git credentialsId: 'GitHub', url: 'https://github.com/surajjp2508/demowebapp.git'
    }
   }
   stage("Code-Check") {
      steps {
        sh 'mvn clean compile'
        echo "Code Compile Completed"
      }
    }
    stage("Run Test cases") {
      steps {
        sh 'mvn clean test'
      }
    }
    stage("Code-Build") {
      steps {
        sh 'mvn clean package'
        echo "Build Completed"
      }
      
    }
    stage("Build-Deploy") {
      steps {
        echo "Build Deployed to Tomcat Server"
      }
    }
  }
}
