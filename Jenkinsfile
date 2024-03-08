pipeline {

    agent any

    tools {
        gradle 'gradle-8.7'
        nodejs 'nodejs21.7'
    }
   
    stages {
        stage('build '){

            steps {
               // echo "build"
                sh 'node -v'
                sh 'npm -v'
             }

        }

    }


}