pipeline {
    agent any

    stages {
        stage ('Code Checkout') {

            steps {
                git changelog: false, credentialsId: 'GitID', poll: false, url: 'https://github.com/DevOpsfirstBatch/jenkins-maven-pipeline'
                }
            }
        

        stage ('Compile') {
            steps {

            withMaven( jdk: 'java1.8', maven: 'maven3.8.6') {
    // some block
                sh "mvn clean compile"
}
            }
        }


        stage ('Test') {
            steps {
                withMaven(jdk: 'java1.8', maven: 'maven3.8.6') {
                sh "mvn test"
}
                }
            
        }
    }
}
