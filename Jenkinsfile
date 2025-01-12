pipeline {
    agent any
    tools {
        maven "MAVEN3"
        jdk "OracleJDK8"
    }

    environment {
        JAVA_HOME = '/usr/lib/jvm/java-8-openjdk-amd64' // Replace with the correct path for JDK 8
        PATH = "${JAVA_HOME}/bin:${env.PATH}"
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin234'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-meven-central'
        NEXUSIP = '172.31.21.228'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = 'vpro-maven-group'
        NEXUS_LOGIN = 'nexuslogin'
    }

    stages {
        stage('Build') {
            steps {
                sh 'mvn -s settings.xml -DskipTests install'
            }
        }
    }
}
