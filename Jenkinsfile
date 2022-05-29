pipeline {
    
    agent any
    tools {
        maven "Maven"
    }
    stages {
        stage("checkoutsc") {
            steps {
             git branch: 'dev', credentialsId: '58cfcb37-f62f-4e01-8040-62a5c6ada73b',  url: "https://github.com/Pavan-971/web-app.git"
             git url: 'https://github.com/naiveskill/devops_cred.git', branch: 'main',
                 credentialsId: 'github_creds'
                
               
            }
        }
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
                    mvn clean
                    mvn package
                    java -jar target/adder-1.0.0.jar
                    '''
               
            }
        }
        
    }
}
