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
                echo "echo 'Building version 5 of the application...'"
                echo "Job Name: ${env.JOB_NAME}"
                echo "Build Number: ${env.BUILD_NUMBER}"
                echo "Workspace: ${env.WORKSPACE}"
                sh 'echo Workspace is: $WORKSPACE'
                sh 'ls -la $WORKSPACE'
                echo "Build URL: ${env.BUILD_URL}"
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