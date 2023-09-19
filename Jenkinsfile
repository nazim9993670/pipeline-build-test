pipeline {
    agent any

    environment {
        
        JAVA_HOME = 'C:/.Net & Java Software/Open JKD -11'    
        MAVEN_HOME = 'C:/.Net & Java Software/apache-maven-3.8.6'  
        PATH = "${JAVA_HOME}\\bin;${MAVEN_HOME}\\bin;${PATH}"
    }

    stages {
        stage('Build') {
            steps {

                //bat 'mvn clean install'
       
                bat 'mvn -f C:/D-A/ss/pipeline-build-test/pom.xml clean install'

            }
        }

        stage('Unit Tests') {
            steps {
                
                //bat 'mvn test'
                
                bat 'mvn -f C:/D-A/ss/pipeline-build-test/pom.xml test'
            }
        }

        stage('Integration Tests') {
            steps {
                
                //bat 'mvn integration-test'

                bat 'mvn -f C:/D-A/ss/pipeline-build-test/pom.xml integration-test'
            }
        }

        stage('Package') {
            steps {

                //bat 'mvn package'

                bat 'mvn -f C:/D-A/ss/pipeline-build-test/pom.xml package'
            }
        }
    }
}

