pipeline {
    agent any
    stages {
          stage('Build') {
            steps {
                git 'https://github.com/Kennetje85/PHPCiCd.git'
                sh 'composer install'
                sh 'cp .env.example .env'
                sh 'php artisan key:generate'
            }       
        }
        stage("Deploy"){
            steps {
            sshPublisher(publishers: [sshPublisherDesc(configName: 'WebserverApache', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: '/var/www/html/', remoteDirectorySDF: false, removePrefix: '', sourceFiles: '**/*.php')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])
            }
        }
    }
}
