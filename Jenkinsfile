
def filename = '${WORKSPACE}/env/dev/deployment.yaml'
def data = readYaml file: filename

def text = "acrlvdevopsuks001.azurecr.io/sr/adisor-portal:1.0.0.${BUILD_NUMBER}"
data.spec.template.spec.containers.image = $text

sh "rm $filename"
writeYaml file: filename, data: data

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

	}


}