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
        stage('AirWatch Agent ') {
          steps {
            echo 'AirWatch Agent '
          }
        }
        stage('AirWatch Agent  Browser') {
          steps {
            echo 'AirWatch Browser'
          }
        }
        stage('Discover Digital ') {
          steps {
            echo 'Discover Digital '
          }
        }
        stage('ANZ Gateway') {
          steps {
            echo 'ANZ Gateway'
          }
        }
        stage('ANZ on Tour') {
          steps {
            echo 'ANZ on Tour'
          }
        }
        stage('GoMoney Demo AU') {
          steps {
            echo 'GoMoney Demo AU'
          }
        }
        stage('GoMoney Demo NZ') {
          steps {
            echo 'GoMoney Demo NZ'
          }
        }
        stage('AtoZ review Small business') {
          steps {
            echo 'AtoZ review Small business'
          }
        }
        stage('AtoZ review Mid Market') {
          steps {
            echo 'AtoZ review Mid Market'
          }
        }
        stage('VoiceNotes') {
          steps {
            echo 'VoiceNotes'
          }
        }
        stage('SuperRegional') {
          steps {
            echo 'SuperRegional'
          }
        }
        stage('ANZ Easy') {
          steps {
            echo 'ANZ Easy'
          }
        }
        stage('Mobi') {
          steps {
            echo 'Mobi'
          }
        }
        stage('Grow for Advice ') {
          steps {
            echo 'Grow for Advice '
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