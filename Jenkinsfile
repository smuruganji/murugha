pipeline {
    agent any
    stages {
        stage('Report') {
            steps {
                sh 'echo "this is oo a report" >> README.md'
                archiveArtifacts allowEmptyArchive: true, artifacts: '*.txt', fingerprint: true, followSymlinks: false, onlyIfSuccessful: true
            }
        }
        stage('cat Readme') {
            steps {
                sh ''' cat README.md '''
                }
            }
        
    }
}
