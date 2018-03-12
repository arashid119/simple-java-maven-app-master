pipeline {
  agent {
    docker {
      args '-v /Users/arashid/.m2:/root/.m2'
      image 'maven:3-alpine'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -e -DskipTests clean install'
      }
    }
     stage('Test') {
            steps {
                sh 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
  }
}