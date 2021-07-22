pipeline {
agent any

tools{
maven "maven-3.8.1"
}

stages {
	stage("Build"){
		steps{

			bat "mvn clean install"
		
			}		
		}
	}


}