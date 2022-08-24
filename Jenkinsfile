pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                git changelog: false, credentialsId: 'GitID', poll: false, url: 'https://github.com/DevOpsfirstBatch/jenkins-maven-pipeline'
                }
            }
        

        stage ('Testing Stage') {

            steps {
               echo "Testing"
                }
            }
        


        stage ('Deployment Stage') {
            steps {
                echo "Deployment"
                }
            
        }
    }
}
