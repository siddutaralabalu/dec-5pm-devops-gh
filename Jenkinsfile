node {
    stage "1. updating jenkins machine"
    sh "sudo yum update -y"
    sh "sudo yum upgrade -y"
    
    stage "2.create some folders"
    sh "mkdir -p devops-5pm"
    sh "mkdir -p besant/devops/6pm-batch"
    
    stage "3. install required packages"
    sh "sudo yum install -y git"
    sh "sudo yum install -y docker"
    sh "sudo yum install -y httpd"
    
    stage "4. restart and enable the services"
    sh "sudo systemctl restart docker"
    sh "sudo systemctl enable docker"
    sh "sudo systemctl restart httpd"
    sh "sudo systemctl enable httpd"
    
    stage "5. view uptime and date"
    sh "date"
    sh "uptime"
    sh "cal 2024"
    
    stage "6. build the code"
    echo "building the code from jenkinsfile in UI"
    
    stage "7. create file"
    sh "touch test.txt"
    
    stage "8. create file and put some data"
    writeFile file:"sample.txt", text: "this is pipeline class"

    stage "9. create folder and  file and put some data"
    sh "mkdir -p testing-cicd"
    writeFile file:"testing-cicd/sample.txt", text: "this is pipeline class"

    stage "10. create docker images"
    sh "docker pull ubuntu"
    sh "docker pull amazonlinux"
    sh "docker pull fedora"
    sh "docker images"
    sh "docker pull centos"
    sh "sudo usermod -a -G docker jenkins"
    sh "sudo systemctl status jenkins"
    sh "sudo systemctl enable jenkins"
} 
