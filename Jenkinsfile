pipeline {
   agent { any { } }

   stages {
      stage('e2e-tests') {
         steps {
            sh 'sudo apt install python3 -y'
            // sh 'source venv/bin/activate'
            sh 'pip install -r requirements.txt'
            sh 'pytest'
         }
      }
   }
}
// pipeline {
//     agent {
//       docker {
//         image 'python:slim'
//         label 'Built-In Node'
//       }
//     }
//     stages {
//         stage('Test') {
//             steps {
//               sh """
//               python --version
//               python ./test.py
//               """
//             }
//         }
//     }
// }