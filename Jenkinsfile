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
        sh 'mvn -B -DskipTests clean install'
      }
    }
  }
}