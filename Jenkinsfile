pipeline{
    agent any

    stages{
        stage('Checkout'){
            steps{
                echo "Getting source code..."
            }
        } 

        stage('build'){
            steps{
                echo "echo 'Building version 2 of the application...'"
            }
        }

        stage('test'){
            steps{
                echo "Testing the application..."
            }
        }

        stage('deploy'){
            steps{
                echo "Deploying the application..."
            }
        }
    }

    post{
        success {
            echo('Pipeline completed successfully')
        }
        
        failure{
            echo('Pipeline failed! Please check the errors.')
        }

        always{
            echo('Pipeline execution is finished.')
        }
    }   
}