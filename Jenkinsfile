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
        sh '''ip a
ls'''
      }
    }

    stage('stage2') {
      steps {
        echo 'stage2'
        sh 'bash x.sh'
      }
    }

  }
}