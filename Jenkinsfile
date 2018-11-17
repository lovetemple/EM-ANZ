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
      }
    }
    stage('publish+tag TC') {
      steps {
        echo 'artifactory Test candidate'
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
    stage('functional tests-staging') {
      parallel {
        stage('functional tests') {
          steps {
            echo 'functional smoke tests'
          }
        }
        stage('app1') {
          steps {
            echo 'app1'
          }
        }
        stage('app2') {
          steps {
            echo 'app2'
          }
        }
        stage('app3') {
          steps {
            echo 'app3'
          }
        }
        stage('app4') {
          steps {
            echo 'app1'
          }
        }
        stage('app5') {
          steps {
            echo 'app5'
          }
        }
        stage('app6') {
          steps {
            echo 'app6'
          }
        }
        stage('app7') {
          steps {
            echo 'app7'
          }
        }
        stage('app8') {
          steps {
            echo 'app8'
          }
        }
        stage('app9') {
          steps {
            echo 'app9'
          }
        }
      }
    }
    stage('report') {
      parallel {
        stage('report') {
          steps {
            echo 'report'
          }
        }
        stage('skype bot report') {
          steps {
            echo 'skype out the report'
          }
        }
        stage('email bot report') {
          steps {
            echo 'email report'
          }
        }
      }
    }
    stage('jira (Zepher/Zapi) integration') {
      steps {
        echo 'jira (Zepher/Zapi) integration traceability'
      }
    }
  }
}