timestamps {

	node('windows') {
		stage('checkout'){
			git credentialsId: 'GITHUB', url: 'https://github.com/kmayer10/ibm-devops-basics-batch-1.git'
		}
		stage('Hello') {
			bat label: '', script: 'echo "[INFO] This is running on Windows"'
		}
	}
		
	node('master') {	
		stage('calling shell'){
		        sh label: '', script: '''#!/bin/bash
                    echo "[INFO] Directly excuting it from Jenkins"
                    echo "[INFO] Directly excuting it from Jenkins" > jenkins.txt
                    echo ${param1} >> jenkins.txt
                    echo ${WORKSPACE} >> jenkins.txt
                    echo ${choice} >> jenkins.txt
                    echo ${GIT_BRANCH}'''		    
		}
		
		stage('echo') {
				echo 'This is Second Stage!'
		}
	}
}
