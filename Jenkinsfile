pipeline {
    agent any
    tools {
        maven 'mvn-3.6.3'
    }
    parameters {

        choice(name:'deployEnv', choices:'dev\ntest\nprod',description: "选择部署环境")
    }
    stages {
        stage("deploy test"){
            when {
                expression {
                    return params.deployEnv == 'test'
                }
            }
            steps{
                echo "部署测试环境：${params.deployEnv}"
            }
        }
        stage("deploy dev"){
            when {
                expression {
                    return params.deployEnv == 'dev'
                }
            }
            steps{
                echo "部署开发环境：${params.deployEnv}"
            }
        }
        stage('deploy prod'){
            when {
                expression {
                    return params.deployEnv == 'prod'
                }
            }
            steps {
                echo "部署正式环境：${params.deployEnv}"
            }
        }
    }
}