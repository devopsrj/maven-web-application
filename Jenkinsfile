node{
    def mvnHome = tool name: 'maven-.3.6.1', type: 'maven'
    
    /*
    stage('checkout code'){
        git branch: 'development', credentialsId: '91f016b4-3022-4e8d-b75b-7daa2d04a0b3', url: 'https://github.com/devopsrj/maven-web-application.git'
    }
    */
    stage('Build'){
     if(isUnix()){
     sh "${mvnHome}/bin/mvn clean package"
      }
      else
      {
       bat "${mvnHome}/bin/mvn clean package"
      }
    }
    /*
    stage('sonarqube report'){
     if(isUnix()){
     sh "${mvnHome}/bin/mvn sonar:sonar"
      }
      else{
       bat "${mvnHome}/bin/mvn sonar:sonar"
        }
    }
    
    stage('upload artifact to nexus'){
        if(isUnix()){
            sh "${mvnHome}/bin/mvn deploy"
        }
            else{
                bat "${mvnHome}/bin/mvn deploy"
            }
   } 
    
    stage('Deploy to tomcat server'){
        if(isUnix()){
            sshagent(['keyID']){ 
    
           sh "scp -o StrictHostKeyChecking=no target/*.war ec2-user@35.154.96.195:/opt/apache-tomcat-9.0.21/webapps/"
        }
        }
        else{
            bat "echo windows"
        }
        }*/
    }


    
