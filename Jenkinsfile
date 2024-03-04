pipeline {
    agent {
        node {
            label 'maven'
        }
    }
environment {
        JAVA_HOME = "/usr/lib/jvm/java-8-openjdk-amd64"
        PATH = "${env.JAVA_HOME}/bin:${env.PATH}"
        MAVEN_HOME = "/opt/apache-maven-3.9.6"
        PATH = "${env.MAVEN_HOME}/bin:${env.PATH}"
}
    stages {
        stage("Build"){
            steps {
               sh 'mvn clean deploy' 
            }
        }
    }
}
