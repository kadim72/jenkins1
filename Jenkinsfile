pipeline {

    agent any


   
    stages {
        stage('build & test'){

            matrix {
                axes {
                    axis {
                        name 'PLATFORM'
                        values 'linux' , 'macOS', 'windows'
                    }
                    axis {
                        name 'BROWSER'
                        values  'firefox', 'chrome', 'safari'
                    }
                }

                stages {

                    stage('build') {
                        steps {

                            echo "construire build  pour ${PLATFORM} - ${ BROWSER }"
                        }
                    }

                    stage('test') {

                    steps {

                            echo "construire test pour ${PLATFORM} - ${ BROWSER }"
                        }
                    }
                }
            }

        }


        stage 'deployment'{

            steps {

                echo 'deploy'
            }

        }
    }


}