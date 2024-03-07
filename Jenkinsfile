pipeline {
        agent any

        parameters {

            booleanParam(name: 'DEPLOY_TO', defaultValue: false, description: 'Deployer en production Yes/No')
 
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
                            equals expected: true, actual: params.DEPLOY_TO
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