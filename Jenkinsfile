pipeline {
   agent any

   stages {
		stage('Checkout') {
			steps {
				git credentialsId: 'GITHUB', url: 'https://github.com/kmayer10/ibm-devops-basics-batch-1.git'
			}
		}
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
