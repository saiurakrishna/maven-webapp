pipeline {
    agent any
    stages {
	  stage('clean WS') {
		steps {
			cleanWs()
		}
	}
        stage('Git checkout') {
            steps {
             git 'https://github.com/saiurakrishna/maven-webapp.git'
            }
        }
        stage('validate') {
            steps {
               sh 'mvn validate'    
               
            }
        }
        stage('compile') {
            steps {
                 
                sh 'mvn compile'
            }
        }
	 stage('test') {
            steps {
                  
                sh 'mvn test'
            }
        }
	 stage('package') {
            steps {
                  
                sh 'mvn package'
            }
        }


    }
}
