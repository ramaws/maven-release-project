def job_name="pipeline_job"
pipeline {
    agent any
    stages {
        stage ('clone'){
            steps {
            git credentialsId: 'git_credentials', url: 'https://github.com/ramaws/maven-release-project.git'
            }
        }
               stage ('verfication') {
            steps {
                sh ''' ls -lrt'''
            }
        }
        stage ('build'){
            tools {
  maven 'maven 3.5.3'
}
            steps {
                sh " mvn clean install"
            }
        }
    }
}
