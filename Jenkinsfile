pipeline {
    stages{
    stage('Initialize'){
        def dockerHome = tool 'docker'
        env.PATH = "${dockerHome}/bin:${env.PATH}"
        }
    }
    agent { docker { image 'maven:3.9.6-eclipse-temurin-17-alpine' } }
  //   tools {
  //   // a bit ugly because there is no `@Symbol` annotation for the DockerTool
  //   // see the discussion about this in PR 77 and PR 52: 
  //   // https://github.com/jenkinsci/docker-commons-plugin/pull/77#discussion_r280910822
  //   // https://github.com/jenkinsci/docker-commons-plugin/pull/52
  //   'org.jenkinsci.plugins.docker.commons.tools.DockerTool' '18.09'
  // }
    stages {
        stage('build') {
            steps {
                echo hello
            }
        }
    }
}
