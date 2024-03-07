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
            input {
                message  'Souhaitez vous deployer en production ?'
                ok 'deployer !'

                submitter 'admin,devops'
                submitParameter 'USER_SUBMIT'
                parameters {
                    string (name: 'VERSION', defaultValue: 'latest' , description: 'Version')
                }

            }

            steps{
                echo "user: ${ USER_VSUBMIT }"
                echo "version: ${ VERSION }"

                echo "deploy  ..."
      
            }
        }
    }


}