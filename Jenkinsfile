pipeline {
    
    agent any  

    stages {

        stage ('Code') {
            steps {
                git url: 'https://github.com/Andy106/aishwarya.git', branch: 'main' 
            }
        }
        
        stage ('Build') { 
            steps {
                echo 'Building Image' 
                bat 'docker build . -t latestproject:latest'
            }
        }
        
        stage ('Run') { 
            steps {
                echo 'Running Container' 
                bat 'docker run -d -p 81:5000 latestproject:latest'

            }
        }

    }
}