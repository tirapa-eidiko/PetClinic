pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'This is a minimal pipeline.' 
            }
        }
        stage('Deploy') {
            steps {
                retry(3) {
				echo 'Deployent mode starts '
                    bat './flakey-deploy'
					
                }

                timeout(time: 3, unit: 'MINUTES') {
                    bat './health-check'
                }
            }
        }
    }
}
