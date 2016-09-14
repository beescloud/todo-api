stage 'build'
   node{
      checkout scm
      sh "mvn -Dmaven.test.failure.ignore=true clean package"
      junit "**/target/surefire-reports/TEST-*.xml"
   }
