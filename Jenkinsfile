pipeline {
	agent any
		stages {
			stage('First') {
				steps {
					/*sh '''
						echo "Step One"
					'''*/
					script {
						env.EXECUTE='true'
					}
				}
			}


			stage('Second') {
				when {
					environment name: 'EXECUTE', value: 'true'
					}
				steps {
					sh '''
						echo "Hello from Test Branch"
					'''
				}
			} 

			stage('Third') {
				when {
					environment name: 'EXECUTE', value: 'false'
					}
				steps {
					sh '''
						echo "Step Three"
					'''
				}
			}
		}
}


