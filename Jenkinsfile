pipeline {
    agent any
    tools {
        jdk "JDK17"
         maven "MAVEN3.9"
    }
    
    environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = 'admin'
        NEXUS_PASS = 'admin234'
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-meven-central'
        NEXUSIP = '172.31.21.667'
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
