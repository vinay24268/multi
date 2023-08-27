pipeline {
    agent any

    stages {
        stage ('Compile Stage') {

            steps {
                withMaven(traceability: true) {
                    sh 'cd /.m2/repository'
                 sh 'mvn clean compile'
                }
            }
        }

        stage ('Testing Stage') {

            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn test'
                }
            }
        }


        stage ('Deployment Stage') {
            steps {
                withMaven(maven : 'maven_3_5_0') {
                    sh 'mvn deploy'
                }
            }
        }
    }
}
