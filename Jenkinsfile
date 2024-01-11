pipeline {
    agent any
    stages {
        stage('helloworld') {
            when {
                branch 'hello'
            }
            steps {
                sh "pip install -r requirements.txt"
                sh 'python3 app.py'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
            }
        }
        stage('calculator') {
            when {
                branch 'main'
            }
            steps {
                sh "pip install -r requirements.txt"
                sh 'python3 app.py'
                input message: 'Finished using the web site? (Click "Proceed" to continue)'
            }
        }
    }
}
