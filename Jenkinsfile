pipeline {
    agent any
 
    stages {
       stage('NPM Setup') {
          steps {
             scripts{
            npm install
             }
             }
       }
        
stage('Adding Android Platform') {
    steps {
       scripts{
          ionic cordova platform add android
       }
        }
    }
      
       stage('Android Build') {
          steps {
                      scripts{
               ionic cordova build android
                      }               
          }
       }

        stage('Publish Android') {
          steps {
              echo "Publish Android"
          }
       }

}
}
