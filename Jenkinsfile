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
                    
					
                }

                timeout(time: 3, unit: 'MINUTES') {
			echo 'Deployent failed due to time out  '
                    
                }
            }
        }
    }
}
sample
