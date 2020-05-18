pipeline {
  agent any
  stages {
    stage('Lint Analysis') {
      steps {
        tool 'gradle-5.4.1-all'
        tool 'JDK8'
        bat 'gradlew.bat lint'
        androidLint()
      }
    }

    stage('Build') {
      steps {
        tool 'gradle-5.4.1-all'
        tool 'JDK8'
        bat 'gradlew.bat build -x lint'
        archiveArtifacts '**/*.apk'
      }
    }

    stage('QARK-SecurityTests') {
      steps {
        sh 'qark --apk ${workspace}\\app\\build\\outputs\\apk\\release\\app-release-unsigned.apk'
        bat 'echo ${workspace}\\app\\build\\outputs\\apk\\release\\app-release-unsigned.apk'
      }
    }

  }
  environment {
    ANDROID_HOME = 'C:\\Program Files (x86)\\Android\\android-sdk'
    JAVA_HOME = 'C:\\Program Files\\Java\\jdk1.8.0_111'
  }
}