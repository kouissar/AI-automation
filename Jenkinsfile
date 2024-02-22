// pipeline {
//    agent { any { } }

//    stages {
//       stage('e2e-tests') {
//          steps {
//             sh 'python -m venv venv'
//             sh 'source venv/bin/activate'
//             sh 'pip install -r requirements.txt'
//             sh 'pytest'
//          }
//       }
//    }
// }
pipeline {
    agent {
      docker {
        image 'python:slim'
        label 'my-build-agent'
      }
    }
    stages {
        stage('Test') {
            steps {
              sh """
              python --version
              python ./test.py
              """
            }
        }
    }
}