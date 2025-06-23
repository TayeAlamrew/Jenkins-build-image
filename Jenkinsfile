pipeline {
	agent any

	stages{

		stage('Build JAR') {
            steps {
                sh 'mvn clean package -DskipTests'
            }
        }
		stage ("build"){
			steps{
				script{
					sh "docker build -t tayealamrew/test-image:0.1 ."

				}
				
			}
		}
		stage('Push Docker Image') {
            steps {
                withCredentials([usernamePassword(credentialsId: 'docker-hub', usernameVariable: 'DOCKER_USER', passwordVariable: 'DOCKER_PASS')]) {
                    sh '''
                        docker push tayealamrew/test-image:0.1
                    '''
                }
            }
        }
	}

	post{

		success{
			echo "Creating and pushing image is successfully done"
		}
    }

}