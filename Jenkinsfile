pipeline {
  agent any
  stages {
    stage('error') {
      steps {
        sleep 1
      }
    }
    stage('build') {
      steps {
        build(job: 'build_job', quietPeriod: 15)
      }
    }
    stage('deploy') {
      steps {
        build 'deploy_job'
      }
    }
    stage('test') {
      steps {
        build 'testing_job'
      }
    }
  }
}