pipeline {
    agent any

    stages {
        stage('Clone Repository') {
            steps {
                git url: 'https://github.com/Abhiofficial-cyber/Firstprogram.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // assuming you have requirements.txt; skip if not
                sh 'pip install -r requirements.txt || echo "No requirements file found"'
            }
        }

        stage('Build') {
            steps {
                // Just a syntax check for Python
                sh 'python -m py_compile *.py'
            }
        }

        stage('Run Application') {
            steps {
                // Replace main.py with your actual Python script if needed
                sh 'python main.py'
            }
        }
    }
}
