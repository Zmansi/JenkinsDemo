pipeline {
    agent any
environment {
JAVA_HOME='/usr/lib/jvm/java-1.8.0-openjdk-amd64'
PATH='/usr/lib/jvm/java-1.8.0-openjdk-amd64/bin:/usr/local/bin:/usr/bin:/bin'
}
    stages {
       stage('NPM Setup') {
          steps {
          sh 'npm install'
         }
       }
        
stage('Adding Android Platform') {
    steps {
       sh 'ionic cordova platform add android--confirm'
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
