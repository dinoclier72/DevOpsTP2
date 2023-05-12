pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'pip install -r requirements.txt'
      }
    }
    stage('test') {
      steps {
        echo  'python test.py'
      }
       post {
        always {
          junit 'test-reports/*.xml'
        }
      }
    }
  }
}
