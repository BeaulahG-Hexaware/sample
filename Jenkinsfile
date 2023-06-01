pipeline {
  stages {
        stage('Build') {
            steps {
                git 'https://github.com/BeaulahG-Hexaware/sample.git'
            }
            }
        stage('Trivy'){
             steps{
                 sh 'trivy image nginx -f json -o trivyreport.json '
             }
             steps{
                 sh 'trivy image --scanners none --image-config-scanners secret nginx '
             }
             steps{
                 sh 'trivy image --scanners none --image-config-scanners config alpine:3.17.0 '

         }
