pipeline {
    agent any
    tools {
        nodejs 'NodeJS'
    }

        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }

        stage('Test') {
            steps {
                sh 'npm test'
            }
        }

        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }

        stage('Deploy') {
            steps {
                bat "del /q /s C:\\inetpub\\wwwroot\\ReactApp\\*"
                 bat "xcopy /E /Y /I build\\* C:\\inetpub\\wwwroot\\ReactApp\\"
            }
        }
    }

    
   
