def version = "1.0.0.${BUILD_NUMBER}"

pipeline {
agent any


stages {
	stage("Build"){
		steps{
			withMaven(maven : 'maven_3_8_1') {

			bat 'mvn clean install'
		
			}
			}		
		}
        stage("update yaml"){
				def filename = '${WORKSPACE}/env/dev/deployment.yaml'
				def data = readYaml file: filename

				data.spec.template.spec.containers.image = acrlvdevopsuks001.azurecr.io/sr/adisor-portal:${version}

				sh "rm $filename"
				writeYaml file: filename, data: data
			}
	}


}