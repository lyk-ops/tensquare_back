def git_auth="713e60e2-ad28-48fb-9f5a-bbb82fccbf9e"
def git_url="git@github.com:lyk-ops/tensquare_back.git"

node {
   stage('拉取代码'){
      checkout([$class: 'GitSCM', branches: [[name: "*/${branch}"]], extensions: [], userRemoteConfigs: [[credentialsId: "${git_auth}", url: "${git_url}"]]])
      
   }
   stage('代码审查') {
      def scannerHome = tool 'sonarqube-scanner'
      withSonarQubeEnv('sonarqube') {
            sh """
                  cd ${project_name}
                  ${scannerHome}/bin/sonar-scanner
               """
}
}
