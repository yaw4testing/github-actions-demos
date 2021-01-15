pipeline {
    agent any
    parameters {
           choice(name: 'version', choices:['1.2', '1.3'], description: '')
    }
    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
        stage('Test') {
            when{
                expression{
                    params.executeTest
                }
            }
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
                echo "deploying versions ${params.Greeting}"
            }
        }
    }
}
