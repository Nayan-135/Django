pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Clone the repository (make sure branch exists)
                git branch: 'main',
                    url: 'https://github.com/Nayan-135/Django'
            }
        }

        stage('Install Dependencies') {
            steps {
                bat 'python -m pip install --upgrade pip'
                bat 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                bat 'python manage.py test'
            }
        }
    }
}
