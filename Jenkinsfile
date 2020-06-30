pipeline {
  agent any
  stages {

    stage('Rollback') {
      steps {
echo 'Rollback completed'
      }
    }

  }
  parameters {
  booleanParam defaultValue: true, description: '', name: 'deleteFile'
  choice choices: ['debug', 'release'], description: '', name: 'type'

}

}
