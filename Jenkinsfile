pipeline {
    agent any
    triggers {  
        pollSCM('H */4 * * *')
    }

    stages {

        stage('build'){

            steps{

                echo "build ..."
      
            }
        }
        stage('deployment production'){
            // input {
            //     message  'Souhaitez vous deployer en production ?'
            //     ok 'deployer !'

            //     submitter 'admin,devops'
            //     submitterParameter 'USER_SUBMIT'
            //     parameters {
            //         string (name: 'VERSION', defaultValue: 'latest' , description: 'Version')
            //     }

            // }
            when {
                branch 'main'
            }

            steps{
                // echo "user: ${ USER_SUBMIT }"
                // echo "version: ${ VERSION }"

                echo "deploy  ..."
      
            }
        }
    }


}