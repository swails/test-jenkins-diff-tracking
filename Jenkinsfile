#!/usr/bin/env groovy

pipeline {
    agent { label 'ansible || linux' }
    stages {
        stage("Interrogate") {
            steps {
                script {
                    echo "I am about to dive into the build object"
                    currentBuild.properties.each {prop, val ->
                        echo "currentBuild.${prop} = ${it}"
                    }
                }
            }
        }
    }
}
