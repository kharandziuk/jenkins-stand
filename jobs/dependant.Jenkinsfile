pipeline {
    agent any
    parameters {
        string(name: 'param1', defaultValue: '', description: 'Greeting message')
    }
    stages {
        stage('Build') {
            steps {
                echo 'peasant say: ${params.param1}'
            }
        }
    }
}
