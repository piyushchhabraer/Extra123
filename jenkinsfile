pipeline {
    agent any

    stages {
        stage('Download data from github acount') {
            steps {
                git 'https://github.com/piyushchhabraer/BADBOY.git'
            }
        }
        stage('Transfer data from Jenkins to Ansible Machine') {
            steps {
                sshPublisher(publishers: [sshPublisherDesc(configName: 'Jenkins', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: 'scp abc.txt 172.60.82.156:/root/abc', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
    }
}
}
}
