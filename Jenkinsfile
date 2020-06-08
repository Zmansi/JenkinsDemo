node {
    agent any
 
    stages {
       stage('NPM Setup') {
                     sh 'npm install'
               }
        
stage('Adding Android Platform') {
sh 'ionic cordova platform add android'
    }
      
       stage('Android Build') {
              sh 'ionic cordova build android'
       }

        stage('Publish Android') {
                       echo "Publish Android"
          
       }

}
}
