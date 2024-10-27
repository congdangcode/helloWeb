pipeline {
    agent any 

    stages {
        stage('Checkout') {
            steps {
                // Kiểm tra mã nguồn từ GitHub
                git 'https://github.com/congdangcode/helloWeb.git'
            }
        }

        stage('Build') {
            steps {
                // Xây dựng dự án (thay đổi lệnh nếu cần)
                sh 'mvn clean package'
            }
        }

        stage('Test') {
            steps {
                // Chạy kiểm thử (thay đổi lệnh nếu cần)
                sh 'mvn test'
            }
        }

        stage('Deploy') {
            steps {
                // Triển khai ứng dụng (thay đổi lệnh nếu cần)
                echo 'Deploying application...'
                // Thêm lệnh triển khai cụ thể của bạn ở đây
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
