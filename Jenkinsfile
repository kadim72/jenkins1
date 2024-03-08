pipeline {

    agent any

    tools {
        gradle 'gradle-8.7'
        nodejs 'nodejs21.7'
    }
   
    stages {
        stage('build '){

            steps {
                echo "build  ..."

        
  
             }

        }

        post {
            success {
                emailext (to: 'mehdikadim72@gmail.com', body:  'test body', subject: 'test subject')
            }
        }

    }


}