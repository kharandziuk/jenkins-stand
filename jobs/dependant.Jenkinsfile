pipeline {
    agent any
    parameters {
        string(name: 'param1', defaultValue: '', description: 'Greeting message')
    }
    node {
      stages {
          stage('Build') {
              steps {
                  script {
                    def name = build.properties.environment.JOB_NAME
                    def queue = jenkins.model.Jenkins.getInstance().getQueue().getItems()
                    if (queue.any{ it.task.getName() == name }) {
                      println "Newer " + name + " job(s) in queue, aborting"
                      build.doStop()
                    } else {
                      println "No newer " + name + " job(s) in queue, proceeding"
                    }
                  }
                  echo 'peasant say: ${params.param1}'
              }
          }
      }
  }
}
