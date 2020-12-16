#!/usr/bin/env groovy
@Library("jenkins_shared_libraries@bugfix/improve-change-detection") _

pipeline {
    agent { label 'ansible || linux' }
    stages {
        stage("Interrogate") {
            steps {
                script {
                    github.interrogateBuild()
                }
            }
        }
    }
}
