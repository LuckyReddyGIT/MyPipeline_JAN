pipeline {
    agent any 
    stages {
        stage('Clone repo and clean it') {
            steps {
                sh "git clone https://github.com/wakaleo/game-of-life.git"
                sh "mvn clean -f game-of-life"
            }
        }
        stage('Test') {
            steps {
                sh "mvn test -f game-of-life"
            }
        }
        stage('Deploy') {
            steps {
                sh "mvn package -f game-of-life"
            }
        }
    }
}
