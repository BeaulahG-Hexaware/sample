pipeline {
  agent any
  stages {
        //stage('Build') {
            //steps {
              //  git 'https://github.com/BeaulahG-Hexaware/sample.git'
            //}
            //}
        stage('Trivy'){
             steps{
                 sh 'trivy image voting-app -f json -o trivyreport.json '
             }
             //steps{
             //    sh 'trivy image --scanners none --image-config-scanners secret voting-app '
            // }
             //steps{
               //  sh 'trivy image --scanners none --image-config-scanners config voting-app '

            //}
        }
  }

}
