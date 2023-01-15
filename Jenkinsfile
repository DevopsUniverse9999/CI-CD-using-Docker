node{
    def buildNumber=BUILD_NUMBER
    stage("Git Clone"){
        git url:'https://github.com/Ayushrp/ci-cd2.git',branch:'master'
    }
    stage("Maven Clean Package"){
        def mavenHome= tool name:"maven",type:"maven" 
        sh "${mavenHome}/bin/mvn clean package"
    }
    stage("Build Docker Image"){
        sh "docker build -t luckymegha/java-web-app-docker:${buildNumber} ."
    }
    stage("Docker Login and Push"){
        withCredentials([string(credentialsId: 'Docker_hub_pwd', variable: 'Docker_hub_pwd')]) {
   
            sh "docker login -u luckymegha -p ${Docker_hub_pwd} "

    }
        sh "docker push  luckymegha/java-web-app-docker:${buildNumber}" 
    }
    stage('Deploy  Application As Docker Container In Docker Deployment server '){

    sshagent(['Docker_Dev_Server_SSSH']) {
        sh "ssh -o StrictHostKeyChecking=no ubuntu@172.31.36.193 docker rm -f javawebappcontainer || true"
    sh "ssh -o StrictHostKeyChecking=no  ubuntu@172.31.36.193 docker run -d -p 8080:8080 --name javawebappcontainer  luckymegha/java-web-app-docker:${buildNumber}"
  }
   }
    }
