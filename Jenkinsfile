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

            withMaven(globalMavenSettingsConfig: 'null', jdk: 'java1.8', maven: 'maven3.8.6', mavenSettingsConfig: 'null') {
    // some block
                sh "mvn clean compile"
}
            }
        }


        stage ('Test') {
            steps {
                withMaven(globalMavenSettingsConfig: 'null', jdk: 'java1.8', maven: 'maven3.8.6', mavenSettingsConfig: 'null') {
                sh "mvn test"
}
                }
            
        }
    }
}
