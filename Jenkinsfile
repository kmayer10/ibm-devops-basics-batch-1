pipeline {
   agent any

   stages {
		stage('Hello') {
			steps {
				echo 'Hello World'
			}
		}
		
		stage('calling shell'){
		    
		    steps{
		        sh label: '', script: '''#!/bin/bash
                    echo "[INFO] Directly excuting it from Jenkins"
                    echo "[INFO] Directly excuting it from Jenkins" > jenkins.txt
                    echo ${param1} >> jenkins.txt
                    echo ${WORKSPACE} >> jenkins.txt
                    echo ${choice} >> jenkins.txt
                    echo ${GIT_BRANCH}'''
		    }
		    
		}
		
		stage('echo') {
			steps {
				echo 'This is Second Stage!'
			}
		}
	}
}
