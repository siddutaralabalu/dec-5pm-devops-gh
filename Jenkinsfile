pipeline {
		agent any
			stages {
				stage ( "1. creating some child folders"){
					steps {
						sh "mkdir -p declarative-pipeline/test"
						sh "mkdir -p jenkins-pipeline-code"
					}
				}
				stage ("2. installing tomcat application") {
					steps {
					   sh "sudo yum update -y"
					   sh "sudo yum install -y tomcat"
					   sh "date"
					   sh "cal 2024"
					   }
					}
				stage ("3. installing java application") {
					steps {
					   sh "sudo yum update -y"
					   sh "sudo yum install -y java"
					   sh "free -m"
					   sh "uptime"
					   }
					}
			}
			
		}
