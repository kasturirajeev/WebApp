node {
      stage ('SCM Checkout'){
      git url: 'https://github.com/kasturirajeev/webapp.git'
}
      stage('Mvn install'){
      def mvnHome = tool name: 'maven3.6.3', type: 'maven'
      def mvnCMD = "${mvnHome}/bin/mvn"
      sh "${mvnCMD} clean install"
      }
      stage('Mvn Compile'){
      def mvnHome = tool name: 'maven3.6.3', type: 'maven'
      def mvnCMD = "${mvnHome}/bin/mvn"
      sh "${mvnCMD} clean compile"
      }
      stage('Mvn Test'){
      def mvnHome = tool name: 'maven3.6.3', type: 'maven'
      def mvnCMD = "${mvnHome}/bin/mvn"
      sh "${mvnCMD} test"
      }
      stage('Mvn Package'){
      def mvnHome = tool name: 'maven3.6.3', type: 'maven'
      def mvnCMD = "${mvnHome}/bin/mvn"
      sh "${mvnCMD} clean package"
      }
      stage ('Mvn Deploy'){
      sh "curl -v -u deployer:deployer -T /var/lib/jenkins/workspace/GitHub-Jenkins-Maven-Tomcat-Pipeline/target/mvn-hello-world.war 'http://52.172.4.141:8082/mvn-hello-world'"
      }      
}
