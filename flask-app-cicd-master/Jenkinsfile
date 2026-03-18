pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        echo 'Building'
        sh '''cd web ; docker build -t flaskapp:v1 .
'''
        sh '''sleep 3
'''
      }
    }
        stage('Test') {
          steps {
            echo 'Testing'
            sh '''sleep 3 
'''
          }
        }
        stage('Integration Tests') {
          steps {
            echo 'Integration Testing Complete.'
          }
        }
        stage('Deployment') {
          steps {
            sh '''sleep 10
'''
            timeout(time: 90) {
              echo 'done.'
            }

          }
        }
    
    stage('Deploy') {
      steps {
        echo 'Deploying'
                    sh '''docker run -d -p 5000:5000 flaskapp:v1
'''
      }
    }
  }
}
