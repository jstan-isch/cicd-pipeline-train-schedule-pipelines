pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                echo 'Running build automation'
                sh './gradlew build'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip',
                    allowEmptyArchieve: true
                fingerprint targets: 'dist/trainSchedule.zip'
            }
        }
    }
}
