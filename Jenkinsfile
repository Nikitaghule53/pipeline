pipeline {
   agent { 
    label {
           label "build-in"
           customWorkspace "/mnt/pipe"
          } 
          }
   stages {
        stage (on-master) {
      steps {
      sh "sudo yum install tree -y"
     } }
         stage (slave-1) {
     agent { 
    label { 
          label "slave1"
          customWorkspace "/mnt/pipe"
}}
   steps {
    sh "yum install httpd"
    sh "yum install docker -y" 
}
}
}}
