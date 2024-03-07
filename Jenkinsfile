pipeline {
    agent any
    triggers {  
        pollSCM('H */4 * * *')
    }

        environment{
            DEPLOY_TO = 'production'
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
                allOf{
                    branch 'main'
                    environment  name: 'DEPLOY_TO', value: 'production' 
                }
            }

            steps{
                // echo "user: ${ USER_SUBMIT }"
                // echo "version: ${ VERSION }"

                echo "deploy  ..."
      
            }
        }
    }


}