pipeline {
    agent any

    stages {

	stage('Preparation') { // for display purposes       
       	    steps {// Get Module One
		
		checkout([  
          $class: 'GitSCM', 
          branches: [[name: '*/master']], 
          doGenerateSubmoduleConfigurations: false, 
          extensions: [[$class: 'RelativeTargetDirectory', relativeTargetDir: '/var/lib/jenkins/jenkins-ws/modules/one']], 
          submoduleCfg: [], 
          userRemoteConfigs: [[url: 'https://github.com/PaNuMo/test-module-one']]
      ])
	    }
	}

    }
}
