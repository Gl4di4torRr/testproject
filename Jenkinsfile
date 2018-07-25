pipeline {

  agent { label 'maven' }

  stages {

    stage('SCM Checkout') {
      steps {
        checkout scm
      }
    }

    stage('git tag') {
    	steps {
    		"""
    			sh git tag v1.0.0-$BUILD_NUMBER && git push origin v1.0.0-$BUILD_NUMBER
    		"""
    	}
    }

 }

}
