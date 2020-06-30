pipeline {
  agent any
  stages {
    stage('Approval') {
      steps {
            input id: 'Rollback', message: 'Do you want to Rollback?', ok: 'Rollback', submitter: 'mitesh'
      }
    }

    stage('Rollback') {
      steps {
echo 'Rollback completed'
      }
    }

  }
  parameters {
  booleanParam defaultValue: true, description: '', name: 'deleteFile'
  choice choices: ['debug', 'release'], description: '', name: 'type'
  credentials credentialType: 'org.jenkinsci.plugins.plaincredentials.impl.StringCredentialsImpl', defaultValue: '', description: '', name: 'sonarToken', required: true
  password defaultValue: '', description: 'Microsoft Azure Credentials', name: 'azureUser'
  string defaultValue: '', description: 'Do you want to rollback?', name: 'rollback', trim: false
  text defaultValue: '', description: 'Release Notes for App Center', name: 'releaseNotes'
}

  environment {
    ANDROID_HOME = 'C:\\Program Files (x86)\\Android\\android-sdk'
    JAVA_HOME = 'C:\\Program Files\\Java\\jdk1.8.0_111'
  }
}
