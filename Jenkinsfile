pipeline {

  agent any

  options {

    buildDiscarder logRotator(artifactDaysToKeepStr: '', artifactNumToKeepStr: '5', daysToKeepStr: '', numToKeepStr: '5')
  }

  stages {
	  stage("checking and testing PR branches"){
		  when {
		  branch "pr*"
		  }
		  steps{
		  echo "Tested all PR branhes"
		  }
	  }
	  stage("checking and testing FIX branches"){
		  when {
		  branch "fix*"
		  }
		  steps{
		  echo "Tested all FIX branhes"
		  }
	  }
	 stage('hello') {
		  steps {
			sh '''

			  python3 demo.py

			'''

		  }

		}
  }
 }
