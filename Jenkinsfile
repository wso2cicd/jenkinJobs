pipeline {
  agent none
  stages {
    stage('wum checkout') {
      steps {
        sh '''export ei_wum_home=/.wum3/products/wso2ei/6.4.0/full/wso2ei-6.4.0/

'''
        sh '''rm -rf $ei_wum_home
'''
        echo 'Need to WUM init'
        sh '''wum update wso2ei-6.4.0
'''
        sh 'export latestWUMZIP=~/.wum3/products/wso2ei/6.4.0/full/$(ls -t |head -n1)'
        sh 'unzip $latestWUMZIP'
      }
    }
  }
  environment {
    wumusername = 'vanji@wso2.com'
  }
}