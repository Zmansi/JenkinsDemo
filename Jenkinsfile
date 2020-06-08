node {
    agent any
 
    stages {
       stage('NPM Setup') {
          steps {
            'npm install'
         }
       }
        
stage('Adding Android Platform') {
    steps {
        'ionic cordova platform add android'
        }
    }
      
       stage('Android Build') {
          steps {
               'ionic cordova build android'
               
          }
       }

        stage('Publish Android') {
          steps {
              echo "Publish Android"
          }
       }

}
}
