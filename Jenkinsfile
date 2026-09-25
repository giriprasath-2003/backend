pipeline  {
     agent any
     
     stages {

        stage('Checkout') {
            steps {
                git branch: 'main',
                    credentialsId: 'git-creds',
                    url: 'https://github.com/giriprasath-2003/backend.git'
            }
         }
         
         stage('Install Dependencies') {
            steps {
                sh '''
                cd ../auth-service_1784011000189 && npm install
                cd ../task-service && npm install
                cd ../notification-service && npm install
                cd ../report-service && npm install
                cd ../api-gateway_1784010924579 && npm install
                '''
            }
        }
      }
   }   
