pipeline {
    agent any
    tools {
        maven 'mvn-3.6.3'
    }
    stages {
        stage('Build'){
            steps {
                script {

                    def browsers = ['chrome','firefox']
                    for (int i=0;i<browsers.size();i++){
                        echo "test the ${browsers[i]}"
                    }

                }
                sh "mvn clean package spring-boot:repackage"
                sh "printev"
            }
        }
    }
}