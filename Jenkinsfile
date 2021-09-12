pipeline {
  agent any
  stages {
    stage('run backup') {
      parallel {
        stage('run backup') {
          steps {
            script {
              gv = load "script.groovy"
            }

          }
        }

        stage('prod') {
          steps {
            sh 'echo "prod"'
          }
        }

      }
    }

  }
  parameters {
    choice(name: 'VERSION', choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
    booleanParam(name: 'executeTests', defaultValue: true, description: '')
  }
}