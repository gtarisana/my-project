pipeline{
    agent any

	stages {

 stage('Getting project from Git') {
            steps{
      			checkout([$class: 'GitSCM', branches: [[name: '*/master']],
			extensions: [],
			userRemoteConfigs: [[url: 'https://github.com/gtarisana/my-project.git']]])
            }
        }

        stage('Cleaning the project') {
            steps{
                sh "npm ci"
            }
        }

        stage('Artifact Construction') {
            steps{
                sh "ng build  "
            }
        }

}

}
