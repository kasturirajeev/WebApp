node {
      stage ('SCM Checkout'){
      git url: 'https://github.com/kasturirajeev/webapp.git'
}
      stage('Mvn install'){
      def mvnHome = tool name: 'Maven3.5.0', type: 'maven'
      def mvnCMD = "${mvnHome}/bin/mvn"
      bat "${mvnCMD} clean install"
      }
      stage('Mvn Compile'){
      def mvnHome = tool name: 'Maven3.5.0', type: 'maven'
      def mvnCMD = "${mvnHome}/bin/mvn"
      bat "${mvnCMD} clean compile"
      }
      stage('Mvn Test'){
      def mvnHome = tool name: 'Maven3.5.0', type: 'maven'
      def mvnCMD = "${mvnHome}/bin/mvn"
      bat "${mvnCMD} test"
      }
      stage('Mvn Package'){
      def mvnHome = tool name: 'Maven3.5.0', type: 'maven'
      def mvnCMD = "${mvnHome}/bin/mvn"
      bat "${mvnCMD} clean package"
      }
}
