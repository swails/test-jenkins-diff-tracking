#!/usr/bin/env groovy
@Library("jenkins_shared_libraries@bugfix/improve-change-detection") _

pipeline {
    agent { label 'ansible || linux' }
    stages {
        stage("Interrogate") {
            steps {
                script {
                    // Comment to force a change
                    def results = github.interrogateBuild()
                    echo "results = ${results}"

                    boolean changed = github.fileChangedIn('.')
                    echo "File changed? ${changed}"
                }
            }
        }
    }
}
