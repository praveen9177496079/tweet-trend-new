pipeline {
    agent {
        node {
            label 'maven'
        }
    }

    stages {
        stage('Hello') {
            steps {
                git branch: 'main', url: 'https://github.com/praveen9177496079/tweet-trend-new.git'
            }
        }
    }
}
