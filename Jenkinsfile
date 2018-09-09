pipeline {
  agent any
  stages {
    stage('stage1') {
      parallel {
        stage('stage1') {
          steps {
            sh '''#!/bin/bash
echo step 1'''
            echo 'Step2 message here'
          }
        }
        stage('stage parrallel to stage1') {
          steps {
            sh 'echo Parallel step'
            echo 'message from parallel stage step 2'
          }
        }
      }
    }
    stage('Stage 2') {
      steps {
        sleep 1
        sh 'echo Stage2'
        echo 'message from stage2'
      }
    }
  }
}