pipeline {

  agent {label 'kubepod'}

  stages {

    stage('Checkout Source') {
      steps {
        git 'https://github.com/ilamtap/ilamtest.git'
      }
    }

    stage('Deploy App') {
      steps {
        script {
          kubernetesDeploy(configs: "nginx.yaml", kubeconfigId: "mykubeconfig")
        }
      }
    }

  }

}
