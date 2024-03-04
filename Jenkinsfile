pipeline {
    agent {
        node {
            label 'maven'
        }
    }
environment {
        JAVA_HOME = "/usr/lib/jvm/java-8-openjdk-amd64"
        MAVEN_HOME = "/opt/apache-maven-3.9.6"
        MVN = "${MAVEN_HOME}/bin"
        JAVA = "${JAVA_HOME}/bin"
}
    stages {
        stage("Build"){
            steps {
               sh 'export PATH=${MVN}:${JAVA}:${PATH}'
               sh 'mvn clean deploy' 
            }
        }
    }
}
