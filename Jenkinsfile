pipeline {

    agent any


   
    stages {
        stage('build '){

            steps {
                sh 'echo hello > word.txt'
                archiveArtifacts(artifacts: '*.txt')

             }

        }

    }


}