pipeline {
  agent none
  stages {
    stage('wum checkout') {
      steps {
        sh '''export ei_wum_home=/.wum3/products/wso2ei/6.4.0/full/wso2ei-6.4.0/
rm -rf $ei_wum_home
#wum init -u -p
wum update wso2ei-6.4.0
export latestWUMZIP=~/.wum3/products/wso2ei/6.4.0/full/$(ls -t |head -n1)
unzip $latestWUMZIP


'''
      }
    }
  }
  environment {
    wumusername = 'vanji@wso2.com'
  }
}