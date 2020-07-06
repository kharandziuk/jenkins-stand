pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo 'King say hello!'
                build job: 'dependant', parameters: [
                    string(name: 'Max', value: "value1")
                ]
            }
        }
    }
}
