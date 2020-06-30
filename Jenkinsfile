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
  credentials credentialType: 'org.jenkinsci.plugins.plaincredentials.impl.StringCredentialsImpl', defaultValue: '', description: '', name: 'sonarToken', required: true
  password defaultValue: '', description: 'Microsoft Azure Credentials', name: 'azureUser'
  string defaultValue: '', description: 'Do you want to rollback?', name: 'rollback', trim: false
  text defaultValue: '', description: 'Release Notes for App Center', name: 'releaseNotes'
}

}
