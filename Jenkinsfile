pipeline {

    agent any


   
    stages {
        stage('build '){

            steps {
                sh 'echo hello > word.txt'
                archiveArtifacs(artifacts: '*.txt')

             }

        }

    }


}