node {
	
	
	def app

	stage("Clone repository"){
		/*clone the repository*/

		checkout scm
	}
	stage("Premissions"){
		/*change directory*/
		sh "cd AdminServer"
		/* set maven wrapper premissions */
		sh "chmod 711 ./mvnw"
	}
	stage("Test"){
		/* run tests if they are there*/
		sh "./mvnw test"
	}
	stage("Build Project"){
		/*get the project and build*/
		sh"./mvnw clean install"
		}
		stage("Build Image"){
			app = docker.build("micknapp79/admin-server")
		}
		stage("Push Image"){
			/* push the image to docker hub */
			sh "echo"
		}
}