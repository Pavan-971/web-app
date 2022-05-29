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
                dir("/var/lib/jenkins/workspace/prj-dum/bb") {
                    sh '''
                    mvn clean
                    mvn package
                    java -jar target/adder-1.0.0.jar
                    '''
                }
               
            }
        }
        
    }
}
