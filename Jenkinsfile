pipeline {
    agent {
		ecs {
            inheritFrom "jenkins-agent"
        }
	}

    stages {
        stage('Checkout Code') {
            steps {
              script {
                    sh 'echo it has been pulled'
                }
                // Using the 'git' step to check out your repository
                //git url: 'https://github.com/insulet-corp-cloud/mongodb-automation'
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'aws sts get-caller-identity --query "Account" --output text'
                }
            }
        }
    }
}
