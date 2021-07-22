pipeline {
agent any

stages {
		steps{

		withMaven(maven : 'maven_3_8_1') {

		bat "mvn clean install"
		}
		}
	}


}