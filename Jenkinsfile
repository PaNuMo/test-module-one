pipeline {
    agent any

    stages {

      stage('Preparation') { // for display purposes
          def MODULE_PATH = "/var/lib/jenkins/jenkins-ws/modules/one"

          steps {// Get Module One
              checkout([
                   $class: 'GitSCM',
                   branches: [[name: '*/master']],
                   extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: MODULE_PATH]],
                   userRemoteConfigs: [[url: 'https://github.com/PaNuMo/test-module-one']]
              ])
	         }
	     }

       stage('Build') {
           steps {
               sh '/var/lib/jenkins/jenkins-ws/gradlew clean deploy'
           }
       }
    }
}
