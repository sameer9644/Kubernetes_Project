pipeline {
  agent { label 'slave'}
  stages {
    stage('Git CheckOut') {
          git 'https://github.com/sameer9644/Kubernetes_Project.git'

      stage('sending file over ssh to the ansible server')
        sshPublisher(publishers: [sshPublisherDesc(configName: 'ansible', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/home/ansible', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '/home/centos/jenkins-workspace/workspace/pro/*')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
      }
    }

  }

