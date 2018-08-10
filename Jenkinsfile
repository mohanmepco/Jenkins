pipeline {
    agent any
tools {
        maven 'apache-maven-3.5.4'
        jdk 'jdk8'
    
    stages {
        stage ('build Stage') {

            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn build'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_4') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
}
