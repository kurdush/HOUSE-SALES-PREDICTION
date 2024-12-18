pipeline {
    agent { 
        node { 
            label 'linux' 
            customWorkspace 'C:\\Users\\kt045427\\Desktop\\jenkins_test' 
        } 
    }

    stages {
        stage('Initialize') {
            steps {
                script {
                    // Install necessary Python packages
                    bat "pip install -r requirements.txt"
                }
            }
        }

        stage('Load and Preprocess Data') {
            steps {
                script {
                    // Run data loading script
                    bat "python data_loading.py"
                }
            }
        }

        stage('Train Model') {
            steps {
                script {
                    // Run model training script
                    bat "python model_training.py"
                }
            }
        }

        stage('Evaluate Model') {
            steps {
                script {
                    // Run model evaluation script
                    bat "python model_evaluation.py"
                }
            }
        }

        stage('Serve Model') {
            steps {
                script {
                    // Start FastAPI server in the background
                    bat 'start /B python model_serving.py'
                    // Wait for the server to start
                    sleep time: 10, unit: 'SECONDS'
                }
            }
        }

        stage('Test Serve Model') {
            steps {
                script {
                    // Test the server with sample values
                    bat '''
                        curl -X POST "http://127.0.0.1:9000/predict" ^
                        -H "Content-Type: application/json" ^
                        -d "{\\"features\\": [13.2, 2.77, 2.51, 18.5, 103.0, 1.15, 2.61, 0.26, 1.46, 3.0, 1.05, 3.33, 820.0]}"
                    '''
                }
            }
        }

        stage('Deploy Model') {
            steps {
                script {
                    // Trigger another Jenkins job for model serving
                    build job: 'ModelServingPipeline', wait: false
                }
            }
        }
    }

    post {
        always {
            archiveArtifacts artifacts: '**.pkl', fingerprint: true
            echo 'Pipeline execution complete.'
        }
    }
}
