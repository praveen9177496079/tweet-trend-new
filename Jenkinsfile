pipeline {
    agent {
        node {
            label 'maven'
        }
    }

    stages ('git clone') {
        stage {
            steps {
                git branch: 'main', url: 'https://github.com/ravdy/tweet-trend-new.git'
            }
        }
    }
}

