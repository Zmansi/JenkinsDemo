pipeline {
    agent any
environment {
JAVA_HOME='/usr/lib/jvm/java-1.8.0-openjdk-amd64'
ANDROID_SDK_ROOT='/home/mansi/Android/Sdk'
ANDROID_HOME='/home/mansi/Android/Sdk'
PATH='/opt/gradle/gradle-3.4.1/bin:/usr/lib/jvm/java-1.8.0-openjdk-amd64/bin:/usr/local/bin:/usr/bin:/bin'

}
    stages {
       stage('NPM Setup') {
          steps {
          sh 'npm install'
         }
       }
        
stage('Adding Android Platform') {
    steps {
       sh 'ionic cordova plugin add cordova-android-support-gradle-release --confirm'
        }
    }
      
       stage('Android Build') {
          steps {
              sh 'ionic cordova build android --confirm'               
          }
       }

        stage('Publish Android') {
          steps {
              echo "Publish Android"
          }
       }

}
}
