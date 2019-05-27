pipeline {
   agent any
   
    tools {
        maven 'localMaven'
    }
    environment {

    PATH = "C:\\WINDOWS\\SYSTEM32"

}

    stages{
        stage('Build'){
            steps {
                bat 'mvn clean package'
                bat 'docker build . -t tomcatwebapp:${env.BUILD_ID}'
            }
        }
    }
}