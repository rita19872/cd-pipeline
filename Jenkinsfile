node {
   def mvnHome
   stage('checkout') { // for display purposes
      //git 'https://github.com/rita19872/sample-maven1.git'
      git 'https://github.com/rita19872/sample-maven2.git'
      env.JAVA_HOME = tool 'JDK1.8'
      mvnHome = tool 'M2'
   }
   stage('Build') {
      if (isUnix()) {
         sh "'${mvnHome}/bin/mvn' clean install"
      } else {
        //  withEnv(['path=G:\\HOME\\App\\;F:\\HOME\\App\\jdk1.8.0_121\\bin;C:\\Program Files\\Java\\jre1.8.0_121\\bin;C:\\Program Files\\Java\\jdk1.8.0_121\\bin;C:\\Python27;G:\\HOME\\install\\Git\\cmd']) {
           bat(/"${mvnHome}\bin\mvn" clean install/)
//}
  
      }
   }
  
}
