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
						echo "Updating Second Stage"
					'''
				}
			} 

			stage('Three') {
				when {
					environment name: 'EXECUTE', value: 'true'
					}
				steps {
					sh '''
						echo "Step Hello"
					'''
				}
			}
		}
}


