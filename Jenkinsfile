pipeline {
  agent {
    docker {
      args '-v /root/.m2:/root/.m2'
      image 'maven:M3_5_2'
    }
    
  }
  stages {
    stage('Build') {
      steps {
        sh 'mvn -B -DskipTests clean package'
      }
    }
  }
}