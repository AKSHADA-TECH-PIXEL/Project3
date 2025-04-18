pipeline {
  agent any
    tools{
      maven 'M2_MAVEN'
          }
   stages {
    stage('Git checkout') {
      steps {
         echo 'This is for cloning the gitrepo'
         git 'https://github.com/AKSHADA-TECH-PIXEL/Project3.git'
                          }
            }
    stage('Create a Package') {
      steps {
         echo 'This will create a package using maven'
         sh 'mvn package'
                             }
            }
            }
    stage('Publish the HTML Reports') {
      steps {
          publishHTML([allowMissing: false, alwaysLinkToLastBuild: false, icon: '', keepAll: false, reportDir: '/var/lib/jenkins/workspace/Banking/target/surefire-reports', reportFiles: 'index.html', reportName: 'HTML Report', reportTitles: '', useWrapperFileDirectly: true])
                        }
            }
}

   
