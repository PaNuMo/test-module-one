pipeline {
    agent any

    stages {

	stage('Preparation') { // for display purposes       
       	    // Get Module One
            dir('/var/lib/jenkins/jenkins-ws/modules/one') {
                git(
                    poll: true,
                    url: 'https://github.com/PaNuMo/test-module-one',
                    branch: 'master'
                )
            }
	}

println('Status LALALALALALALALALALALLA ')	   
    }
}
