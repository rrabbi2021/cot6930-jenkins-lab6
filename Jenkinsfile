pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                sh '''
                echo "Build Step: No compilation needed for Python project"
                '''
            }
        }

        stage('Test') {
            steps {
                sh '''
                echo "Running tests with pytest"

                # Create virtual environment (safe and standard)
                python3 -m venv venv
                . venv/bin/activate

                # Install dependencies
                pip install --upgrade pip
                pip install pytest numpy pandas scikit-learn

                # Run tests
                pytest -v
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy Step: No deployment required for this lab"
                echo "In real projects, this would publish artifacts or models"
            }
        }
    }
}