pipeline {
    agent any

    stages {

        stage('Build') {
            steps {
                bat '''
                echo Build Step: No compilation needed
                '''
            }
        }

        stage('Test') {
            steps {
                bat '''
                echo Running tests...

                python -m venv venv
                call venv\\Scripts\\activate

                pip install --upgrade pip
                pip install pytest numpy pandas scikit-learn

                pytest -v
                '''
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploy step not required"
            }
        }
    }
}