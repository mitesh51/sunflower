pipeline {
  agent any
  stages {
    stage('Lint Analysis') {
      steps {
        tool 'gradle-5.4.1-all'
        tool 'JDK8'
        bat 'gradlew.bat lint'
      }
    }

    stage('Build') {
      steps {
        tool 'gradle-5.4.1-all'
        tool 'JDK8'
        bat 'gradlew.bat build'
        junit '**/build/test-reports/*.xml'
        archiveArtifacts '**/*.apk'
      }
    }

  }
  environment {
    ANDROID_HOME = 'C:\\Program Files (x86)\\Android\\android-sdk'
    JAVA_HOME = 'C:\\Program Files\\Java\\jdk1.8.0_111'
  }
}