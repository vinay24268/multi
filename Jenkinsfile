pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(traceability: true) {
                 sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(traceability: true) {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(traceability: true) {
                    sh 'mvn install'
                }
            }
        }
    }
}
