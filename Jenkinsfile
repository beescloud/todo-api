stage 'build'
   node{
      checkout scm
      sh "mvn -Dmaven.test.failure.ignore=true clean package"
      junit "**/target/surefire-reports/TEST-*.xml"
   }

stage 'test'
   parallel integration : {
      echo "integration tests tests"
   }, functional: {
      echo "functional tests"
   }

stage 'deploy'
	echo "deploy"