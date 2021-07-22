pipeline {
agent any

tools{
maven "M3"
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