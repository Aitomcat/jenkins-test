pipeline {
    agent any
    stages {
        stage('Verify Branch') {
            steps {
                echo "当前分支: ${env.BRANCH_NAME}"
            }
        }
        stage('Simulate Build') {
            steps {
                sh '''
                    echo "构建号: ${BUILD_NUMBER}"
                    echo "工作区: $(pwd)"
                    echo "文件列表:"
                    ls -la
                '''
            }
        }
    }
    post {
        always {
            echo "流水线结束，分支: ${env.BRANCH_NAME}"
        }
    }
}
