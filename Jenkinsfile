pipeline {
       agent {
                docker {image 'node'
                        args '-u root:root'
                        reuseNode true
                        }
            }
    stages {
        stage('clone') {
        
            steps {
                
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/devopsPRO27/kub']]])
                sh 'whoami'
            }
        }
        stage('build') {
        
            steps {
                sh 'node -v'
                sh 'npm install'
                
                
            }
        }       
       

    }
   
}
    
