/* Requires the Docker Pipeline plugin */
pipeline {
    agent { docker { image 'maven:3.9.8-eclipse-temurin-21-alpine' } }
    stages {
        stage('build') {
		steps {
			sh 'mvn --version'
		}
        }
	stage('test') {
		steps {
			sh 'echo \'running tests...\''
		}
	}
	stage('deploy - staging') {
		steps {
			sh 'echo \'deploying to staging...\''
		}
	}
	stage('sanity check') {
		steps {
			input 'does the staging environment look ok?'
		}
	}
	stage('deploy - production') {
		steps {
			sh 'echo \'deploying to production...\''
		}
	}
    }
}