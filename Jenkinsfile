pipeline {
agent any


stages {
	stage("Build"){
		steps{
			withMaven(maven : 'maven_3_8_1') {

			mvn clean install
		
			}
			}		
		}
	}


}