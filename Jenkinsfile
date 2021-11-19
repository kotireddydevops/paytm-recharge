node {
    
     stage('pulling code from scm'){
       git credentialsId: 'git-hub', url: 'https://github.com/kotireddydevops/paytm-recharge.git'  
     }
     
     stage('list of files in scm'){
         sh 'ls'
     }
     
     stage('build step'){
         sh 'mvn clean install'
     }
     
     stage('delete old artifact'){
         sh 'sudo rm -rf /opt/tomcat9/webapps/recharge.war'
     }
     
     stage('copy artifact'){
         sh 'sudo cp -rf /var/lib/jenkins/workspace/pipelinejob-1/target/recharge.war /opt/tomcat9/webapps/'
     }
}
