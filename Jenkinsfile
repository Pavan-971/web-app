pipeline {
    
    agent any
    tools {
        maven "Maven"
    }
    stages {
        stage("Intialization") {
            steps {
                sh '''    
                echo "PATH = ${PATH}"
                echo "M2_PATH = ${M2_PATH}"
            
                '''
            }
            
        }
        stage("build") {
            steps {
                sh '''
                mvn package
                '''
            }
        }
        
    }
}
