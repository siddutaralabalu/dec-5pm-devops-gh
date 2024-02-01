pipeline {
    agent any
    
    stages {
        stage ("1. updating system") {
            steps {
               sh  "sudo yum update -y"
               sh "sudo yum install -y tomcat"
            }
        }    
        stage ("2. install some packages") {
            steps {
                sh "sudo yum install java"
                sh "sudo yum install -y python3"
            }
        }
        stage ("3. create some files and folders") {
            steps {
                sh "sudo mkdir -p test"
                sh "sudo touch declarative.txt"
            }
        }
        
        stage ("4. view memory") {
            steps {
                sh "sudo free -m"
                sh "lsblk"
            }
        }
        
        stage ("5.view permissions of the file") {
            steps {
                sh "sudo ls -al"
                sh "sudo df -h"
            }
        }
    
    }
}
