pipeline {
    agent any
    tools {
        maven 'mvn-3.6.3'
    }
    stages {
        stage('Build'){
            steps {
//                script {
//
//                    def browsers = ['chrome','firefox']
//                    for (int i=0;i<browsers.size();i++){
//                        echo "test the ${browsers[i]}"
//                    }
//
//                }
//                sh "mvn clean package spring-boot:repackage"
                sh "printenv"
            }
        }
        stage("环境变量") {
            steps {
                echo "Runing ${env.BUILD_NUMBER} on ${env.JENKINS_URL}"
                echo "Runing ${env.BRANCH_NAME} "
            }
        }
    }
}