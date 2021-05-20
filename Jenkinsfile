pipeline {
	agent any
		stages {
			stage('First') {
				steps {
					/*sh '''
						echo "Step One"
					''' */
					script {
						env.EXECUTE="True"
					}

				}
			}


			stage('Second') {
				when {
					${EXECUTE}="True"
					}
				steps {

					sh '''
						echo "Updating Second Stage"
					'''}
					
				}
			} 

			stage('Third') {
				steps {
					sh '''
						echo "Step Three"
					'''
				}
			}
		}
}

