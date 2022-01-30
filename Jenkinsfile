pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'docker build -t hello-world-php-apache .'
                sh 'docker run -d -p 8084:80 hello-world-php-apache'
            }
        }
	    stage('Test') {
		    steps {
			    sh 'wget http://localhost:8084/'
		    }
	    }
    }
}
