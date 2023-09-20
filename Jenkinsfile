pipeline {
    agent none
    stages {
        stage("parallelpipe") {
            parallel {
                stage("one") {
                    agent { label 'label1' }
                    steps {
                       echo "Hello label1"
                    }
                }
                stage("two") {
                    agent {
                        label 'label2'
                    }
                    steps {
                       echo "Hello label2"
                    } 
                }
              stage("three") {
                    agent any
                    steps {
                       echo "Hello label3"
                    } 
                }
            }
        }
    }
}
