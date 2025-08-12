pipeline {
    agent any

    triggers {
        // This is for webhook or polling — comment/uncomment based on your setup
        // Polling example: pollSCM('H/5 * * * *')
    }

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main', url: 'https://github.com/yourusername/yourrepo.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                sh 'echo "Installing dependencies..."'
                // Example for Python: sh 'pip install -r requirements.txt'
                // Example for Node:   sh 'npm install'
            }
        }

        stage('Run Automation Script') {
            steps {
                sh 'echo "Running automation script..."'
                // sh 'bash automation.sh' // Replace with your script
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
