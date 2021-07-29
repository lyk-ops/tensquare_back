def git_auth:713e60e2-ad28-48fb-9f5a-bbb82fccbf9e
def git_url:git@github.com:lyk-ops/tensquare_back.git

node {
   stage('拉取代码'）{
      checkout([$class: 'GitSCM', branches: [[name: '*/v1']], extensions: [], userRemoteConfigs: [[credentialsId: "${git_auth}", url: "${git_url}"]]])
   }
}
