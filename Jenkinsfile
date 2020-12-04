pipeline {
  agent {
    node {
      label 'worker'
    }

  }
  stages {
    stage('stage1') {
      parallel {
        stage('stage1.1') {
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

        stage('stage1.2') {
          steps {
            build 'proj1'
          }
        }

        stage('stage1.3') {
          steps {
            echo 'in stage1.3'
          }
        }

      }
    }

    stage('stage2') {
      parallel {
        stage('stage2.1') {
          steps {
            echo 'stage2'
            sh 'bash x.sh'
          }
        }

        stage('stage2.2') {
          steps {
            build 'proj2'
          }
        }

      }
    }

  }
}