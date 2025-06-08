pipeline {
	agent any

	stages{
		stage ("build"){
			steps{
				echo "build"
			}
		}
		stage ("test"){
			steps{
				echo "test"
			}
		}
		stage ("integration test"){
			steps{
				echo "integration test"
			}
		}
	}

	post{
		always{
			echo "always"
		}
		failure{
			echo "failure"
		}
		success{
			echo "success"
		}
	}

}