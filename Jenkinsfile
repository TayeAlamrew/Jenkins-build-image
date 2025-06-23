pipeline {
	agent any

	stages{
		stage ("build"){
			steps{
				sh "docker build -t tayealamrew/test-image:0.1 ."
			}
		}
		stage ("Push"){
			steps{
				sh "docker push tayealamrew/test-image:0.1"
			}
	    }
	}

	post{

		success{
			echo "Creating and pushing image is successfully done"
		}
    }

}