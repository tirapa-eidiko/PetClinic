pipeline {
agent { docker 'maven:3.3.3' }
stages {
stage('build') {
steps {
bat 'mvn --version'
}
}
}
post {
always {
bat 'This will always run'
}
success {
bat 'This will run only if successful'
}
failure {
bat 'This will run only if failed'
}
unstable {
bat 'This will run only if the run was marked as unstable'
}
changed {
bat 'This will run only if the state of the Pipeline has changed'
bat 'For example, the Pipeline was previously failing but is now successful'
}
}

}

