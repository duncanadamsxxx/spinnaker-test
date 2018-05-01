node('master') {
    checkout scm
    sh "ls -l"
    //s3Upload consoleLogLevel: 'INFO', dontWaitForConcurrentBuildCompletion: false, entries: [[bucket: 'demo-repo-spinnaker', excludedFile: '', flatten: false, gzipFiles: false, keepForever: false, managedArtifacts: true, noUploadOnFailure: false, selectedRegion: 'us-east-1', showDirectlyInBrowser: false, sourceFile: '*.java', storageClass: 'STANDARD', uploadFromSlave: false, useServerSideEncryption: false]], pluginFailureResultConstraint: 'FAILURE', profileName: 'artifactpublisher', userMetadata: []
}
