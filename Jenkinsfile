pipeline {
    
	agent any
	
	tools {
        maven "Maven3"
        jdk "OracleJDK8"
    }
	
	environment {
        SNAP_REPO = 'vprofile-snapshot'
        NEXUS_USER = "admin"
        NEXUS_PASS= "admin007"
        RELEASE_REPO = 'vprofile-release'
        CENTRAL_REPO = 'vpro-maven-central'
        NEXUSIP = '172.31.4.113'
        NEXUSPORT = '8081'
        NEXUS_GRP_REPO = "vprofile-maven-group"
        NEXUS_CREDENTIAL_ID = "nexuslogin"
        NEXUS_LOGIN = 'nexuslogin'
    }
	
    stages{
        
        stage('Build'){
            steps {
                sh 'mvn -s setting.xml -DskipTests install'
                
            }
        }

    }


}