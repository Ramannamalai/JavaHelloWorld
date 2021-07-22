pipeline {
agent any

tools{
apache-maven-3.8.1
}

stages {
stage("Build") {
steps {
git 'https://github.com/Vignesh2793/JavaHelloWorld'

bat "mvn clean install"
}
}
}


}