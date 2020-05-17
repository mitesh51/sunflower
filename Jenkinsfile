pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        bat 'gradlew.bat clean build'
      }
    }

  }
  environment {
    ANDROID_HOME = 'C:\\Program Files (x86)\\Android\\android-sdk'
  }
}