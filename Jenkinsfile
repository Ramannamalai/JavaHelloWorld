
pipeline {
agent any

environment{

version = "1.0.0.${BUILD_NUMBER}"

}

stages {

    stage("update yaml"){
				steps{
				script{
				def data = readYaml file:"${WORKSPACE}/env/dev/deployment.yaml"
				
				data.spec.containers.image = "acrlvdevopsuks001.azurecr.io/sr/adisor-portal:$version"

				writeYaml file: "${WORKSPACE}/env/dev/deployment.yaml", data: data
				}
			}
			
	}
}
}