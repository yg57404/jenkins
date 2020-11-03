pipeline {
  agent any
    
  tools {nodejs "node"}
    
  stages {
        stage('Deploy') {
          steps{
        sh 'curl -sL https://rpm.nodesource.com/setup_12.x | sudo -E bash - '
        sh 'sudo yum install npm -y'  
        sh 'cd /var/www/html; [ -d "/var/www/html/js" ] && sudo git pull || sudo git clone git@github.com:yg57404/js.git'
        sh 'sudo cd /var/www/html/js;npm install'
        sh 'sudo cd /var/www/html/js;npm start &'
     }
   }
 }
}
