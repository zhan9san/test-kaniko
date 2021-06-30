pipeline {
  agent {
    kubernetes {
      yamlFile 'kubernetes-plugin/KubernetesPod.yaml'
    }
  }
  stages {
    stage('Build') {
      steps {
        container('kaniko') {
          sh 'pwd; ls -la'
        }
      }
    }
  }
}
