
pipeline {
agent any

environment{

version = "1.0.0.${BUILD_NUMBER}"
filename = "${WORKSPACE}/env/dev/deployment.yaml"
data = readYaml file: filename

}

stages {
	stage("Build"){
		steps{
			withMaven(maven : 'maven_3_8_1') {

			bat 'mvn clean install'
		
			}
			}
		}
    stage("update yaml"){
				steps{
				script{
				data.spec.template.spec.containers.image = "acrlvdevopsuks001.azurecr.io/sr/adisor-portal:$version"
				sh "rm ${filename}"
				writeYaml file: "${filename}", data: data
				}
			}
			
	}
}
}