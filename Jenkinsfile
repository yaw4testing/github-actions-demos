pipeline {
    agent any
    parameters {
            choice(name: 'version', choices: ['version 1.1','version 1.2','version 1.3'], description: 'build versions')
            booleanValues(name: 'executeTest', defaultValue =true)
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
                echo "deploying version ${params.version}"
            }
        }
    }
}
