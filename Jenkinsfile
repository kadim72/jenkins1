pipeline {

    agent any


   
    stages {
        stage('build'){

            failFast true

            parallel {

                            stage('build frontend '){

                    steps{

                        echo "build frontend..."
            
                    }
            }
           stage('build backend '){

                    steps{

                        echo "build backend..."
            
                    }
            }

            }

        }
        stage('deployment production'){
             parameters {

                     booleanParam(name: 'DEPLOY_TO', defaultValue: false, description: 'Deployer en production Yes/No')

                }
   
                when {
                    allOf{
                        branch 'main'
                        equals expected: true, actual: params.DEPLOY_TO
                    }
                }

                steps{

                    echo "deploy  ..."      
                }
        }
    }


}