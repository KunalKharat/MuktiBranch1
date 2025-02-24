pipeline {
    agent any

    stages {
        stage('First') {
            steps {
                echo "This is the First Step. ${env.BRANCH_NAME}"
            }
        }
        stage('Second') {
            steps {
                echo "Second Step."
            }
        }
        stage('Third') {
            steps {
                when {
                    expression { env.BRANCH_NAME == master }
                }
                echo " This is a ${env.BRANCH_NAME} "
            }
	    	when {
		    expression { env.BRANCH_NAME == feature }
		}
		echo " This is a not a Master Branch "
        }
    }
}

