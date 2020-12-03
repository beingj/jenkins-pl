pipeline {
  agent {
    node {
      label 'worker'
    }

  }
  stages {
    stage('stage1') {
      agent {
        node {
          label 'worker'
        }

      }
      steps {
        sh 'hostname'
        node(label: 'worker') {
          echo 'allocate worker'
        }

      }
    }

  }
}