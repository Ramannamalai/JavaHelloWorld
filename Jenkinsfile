pipeline {
agent any

stages {
	stage("Build"){
		steps{

		withMaven(maven : 'maven_3_8_1') {

		bat "mvn clean install"
		}
		}		
		}
	}


}