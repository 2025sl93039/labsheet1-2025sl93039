pipeline {
    agent any

    stages {
	stage('Checkout') {
            steps {
                git 'https://github.com/2025sl93039/labsheet1-2025sl93039.git'
            }
	}

	stage('Build') {
            steps {
                sh 'echo "Building project..."'
                sh 'python3 --version'
            }
	}

	stage('Test') {
            steps {
                sh '''
                python3 - <<EOF
import calculator

assert calculator.add(2,3) == 5
assert calculator.subtract(5,3) == 2
assert calculator.multiply(2,3) == 6
assert calculator.divide(6,2) == 3

print("All tests passed")
EOF
                '''
            }
	}

	stage('Deploy') {
            steps {
                sh 'echo "Deploy stage (placeholder)"'
            }
	}
    }
