pipeline {
  agent any
  stages {
    stage('checkout') {
      steps {
        echo 'check out code'
      }
    }
    stage('compile') {
      steps {
        echo 'compiled code'
      }
    }
    stage('verify compile') {
      parallel {
        stage('verify compile') {
          steps {
            echo 'check style analysis'
          }
        }
        stage('findbug analysis') {
          steps {
            echo 'findbug analysis'
          }
        }
        stage('PMD source analyser') {
          steps {
            echo 'PMD source analyser'
          }
        }
      }
    }
    stage('local unit tests') {
      parallel {
        stage('local tests') {
          steps {
            echo 'local unit tests'
          }
        }
        stage('software composition analysis') {
          steps {
            echo 'software composition analysis'
          }
        }
      }
    }
    stage('post compile') {
      parallel {
        stage('post compile') {
          steps {
            echo 'post compile'
          }
        }
        stage('unit test coverage') {
          steps {
            echo 'test coverage'
          }
        }
      }
    }
    stage('fortify scan') {
      steps {
        echo 'fortify scan'
      }
    }
    stage('verify assemble') {
      parallel {
        stage('verify assemble') {
          steps {
            echo 'verify assemble'
          }
        }
        stage('integration tests') {
          steps {
            echo 'integration tests'
          }
        }
        stage('performance tests') {
          steps {
            echo 'performance tests'
          }
        }
      }
    }
    stage('publish+tag RC') {
      steps {
        echo 'artifactory release candidate'
      }
    }
    stage('deploy to staging') {
      parallel {
        stage('deploy to staging') {
          steps {
            echo 'deploy to staging'
          }
        }
        stage('monitor app health') {
          steps {
            echo 'monitor app health'
          }
        }
      }
    }
  }
}