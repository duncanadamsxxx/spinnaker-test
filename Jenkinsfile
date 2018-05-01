pipeline {
    agent { label "master" }
    tools {
        maven 'M3'
    }
    stages {
        stage("build artifact") {
	    steps{
    checkout scm
    sh "ls -l"
    sh "mvn package"
    //s3Upload consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'demo-repo-spinnaker', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: true, noUploadOnFailure: false, selectedRegion: 'us-east-1', showDirectlyInBrowser: false, sourceFile: '*.java', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 'artifactpublisher', userMetadata: []
    sh "ls -l target/"
    }
   }
  }
  post {
      always {
          sh "deb-s3 upload --bucket demo-repo-spinnaker --arch amd64 --codename trusty --preserve-versions true target/*.jar"
	  }
	}
}
    
    
    
