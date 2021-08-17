pipeline {
    agent any
    parameters {
    string(name: 'PERSON', defaultValue: 'jstan-isch', description: 'Running build automation on jenkins server')
    }

    stages {
        stage('build') {
            steps {
                echo "${params.PERSON} - to deploy train-schedule application on Jenkins Master"
                echo 'Running build automation'
                sh './gradlew build'
                archiveArtifacts artifacts: 'dist/trainSchedule.zip',
                    allowEmptyArchieve: true
                fingerprint targets: 'dist/trainSchedule.zip'
            }
        }
    }
}
