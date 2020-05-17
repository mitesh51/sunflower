pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        tool 'gradle-5.4.1-all'
        bat 'gradlew.bat assembleDebug'
      }
    }

  }
  environment {
    ANDROID_HOME = 'C:\\Program Files (x86)\\Android\\android-sdk'
  }
}