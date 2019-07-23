Jenkinsfile (Declarative Pipeline)
pipeline {
    agent {
        label '10.112.19.157'
    }
    stages {
        stage('Build') {
            steps {
                bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Wutao Test') {
            steps {
                bat 'echo aaaaaaaa'
                bat "D:\\code\\test.bat"
                bat 'mvn -B -DskipTests clean package'
            }
        }
        stage('Test') {
            steps {
                bat 'mvn test'
            }
            post {
                always {
                    junit 'target/surefire-reports/*.xml'
                }
            }
        }
    }
}