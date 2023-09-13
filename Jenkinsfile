pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'Installing dependencies..'
                sh 'python3 -m pip install pytest'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'pytest test_add.py'
            }
        }
    }
}
```