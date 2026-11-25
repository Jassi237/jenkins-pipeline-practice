pipeline{
    agent any

    environment{
        APP_NAME = 'my-app'
        VERSION = '1.0'
    }

    stages{
        stage('Checkout'){
            steps{
                echo "Getting source code..."
            }
        } 

        stage('build'){
            steps{
                echo "Building: ${env.APP_NAME}"
                sh 'echo "Testing $APP_NAME version $VERSION"'
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