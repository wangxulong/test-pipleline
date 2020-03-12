pipeline {
    agent any
    tools {
        maven 'mvn-3.6.3'
    }
    parameters {
        booleanParam(defaultValue:true, description:'', name:"userFlag")
        string(defaultValue:'staging', description:'', name:"deploy_env")
        text(defaultValue:'one\nTwo\nThree', description:'', name:"deploy_text")
        choice(name:'choice', choices:'dev\ntest\nprod',description: "选择部署环境")
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

            }
        }

        stage("参数化") {
            steps{
                echo "答应参数"
                echo "flag:${params.userFlag}"
                echo "deploy_env:${params.deploy_env}"
                echo "deploy_text:${params.deploy_text}"
                echo "选择部署环境:${params.choice}"
            }
        }
    }
}