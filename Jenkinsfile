pipeline {
  agent any
  stages {
        //stage('Build') {
            //steps {
              //  git 'https://github.com/BeaulahG-Hexaware/sample.git'
            //}
            //}
        stage('Trivy') {
             steps{
                 sh 'trivy image voting-app -f json -o trivyreport.json '
                 sh 'trivy image --image-config-scanners config voting-app -f json -o trivyconfig.json '
                 sh ' trivy image --scanners none --image-config-scanners config voting-app -f json -o trivysecret.json '
                 sh ' trivy fs --scanners vuln,secret,config /home/kali/example-voting-app/ -f json -o trivyfs.json '

            }
        }
     }
  }
