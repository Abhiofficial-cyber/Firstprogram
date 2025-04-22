pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                git url: 'https://github.com/Abhiofficial-cyber/Firstprogram.git', branch: 'main'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh '''
                    if [ -f requirements.txt ]; then
                        python3 -m pip install -r requirements.txt
                    else
                        echo "No requirements file found"
                    fi
                '''
            }
        }

        stage('Build') {
            steps {
                sh 'python3 -m py_compile hello.py'
            }
        }

        stage('Run Application') {
            steps {
                sh 'python3 hello.py'
            }
        }
    }
}
