pipeline {
    agent any
    parameters {
        string(name: 'param1', defaultValue: '', description: 'Greeting message')
        string(name: 'param2', defaultValue: '', description: '2nd parameter')
    }
    stages {
        stage('Build') {
            steps {
                echo 'King say hello!'
                build job: 'peasant', parameters: [
                    string(name: 'Max', value: "value1")
                ]
            }
        }
    }
}
