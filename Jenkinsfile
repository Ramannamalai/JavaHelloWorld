
pipeline {
agent any

environment{

version = "1.0.0.${BUILD_NUMBER}"

}

stages {

    stage("update yaml"){
				steps{
				script{
				def data = readYaml file:"C:\\Users\\sugheerth\\Documents\\deployment.yaml"
				
				data.steps.build-example.type = "acrlvdevopsuks001.azurecr.io/sr/adisor-portal:$version"

				writeYaml file: "C:\\Users\\sugheerth\\Documents\\deployment1.yaml", data: data
				}
			}
			
	}
}
}