pipeline {
    agent any

    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
            }
        }
        stage('Step 1') {
            steps {
                echo 'Step 1'
                sh "uname"
            }
        }
        stage('Step 2') {
            steps {
                echo 'Step 2'
                sh "java --version"
            }
        }
        stage('Step 3') {
            steps {
                echo 'Test sonar 3'
                sh "mvn sonar:sonar \
                    -Dsonar.projectKey=test-maven \
                    -Dsonar.host.url=http://localhost:8084 \
                    -Dsonar.login=2780c61dc2947718dcba435f8210a0bfbac94f26"
            }
        }
        stage('Step 4') {
            steps {
                echo 'Step 4'
                sh "pwd"
            }
        }
        stage('Good Bye') {
            steps {
                echo 'Good Bye Usach Ceres'
            }
        }
    }
}