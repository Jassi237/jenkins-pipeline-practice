pipeline{
    agent any

    environment{
        APP_NAME = 'my-app'
        VERSION = '1.0'
    }

    parameters{
        string(
            name: 'APP_VERSION',
            defaultValue: '1.0',
            description: 'Enter the application version'
        )
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
                echo "Version: ${params.APP_VERSION}" 
            }
        }

        stage('test'){
            steps{
                echo "Testing ${env.APP_NAME} version ${params.APP_VERSION}"
            }
        }

        stage('deploy'){
            steps{
                echo "Deploying ${env.APP_NAME} version ${params.APP_VERSION}"
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