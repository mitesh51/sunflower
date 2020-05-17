pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        tool 'gradle-5.4.1-all'
        tool 'JDK8'
        bat 'gradlew.bat assembleDebug'
      }
    }

  }
  environment {
    ANDROID_HOME = 'C:\\Program Files (x86)\\Android\\android-sdk'
    JAVA_HOME = 'C:\\Program Files\\Java\\jdk1.8.0_111'
  }
}