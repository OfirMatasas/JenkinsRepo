pipeline {
    agent {
        docker { image 'python_with_pytest:latest' }
    }
    stages {
        stage('Test and Sleep') {
            parallel {
                stage('Test') {
                    steps {
                        echo 'Testing..'
                        sh 'python3 -m pytest test_add.py'
                    }
                }
                stage('Sleep and Count') {
                    steps {
                        script {
                            for (int i = 1; i <= 10; i++) {
                                echo "Sleeping... Count ${i}"
                                sh 'sleep 1'
                            }
                        }
                    }
                }
            }
        }
    }
}
