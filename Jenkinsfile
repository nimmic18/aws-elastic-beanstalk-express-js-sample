pipeline {
    agent {
        docker {
            image 'node:16-alpine' // Use node 16 Alpine Docker image to run the pipeline
        
        }
    }

        stages { 
            stage('Install Dependencies') {
            steps {
                script {
                    // Install npm dependencies
                    sh 'npm install --save'
                }
            }
        }

         stage('Test') {
      steps {
        sh 'node --12.22.9'
        sh 'echo "Testing the application."'
         snykSecurity(
          snykInstallation: 'snyk@latest',
          snykTokenId: 'snyk-api-token',
         // snyktest: '--severity-threshold=medium|high', // Will accept medium or high vulnerabilities but exit on critical vulnerabilities
         )
      }
    }
    }
}
