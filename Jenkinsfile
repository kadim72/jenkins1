pipeline {
    agent any

    environment{

        MY_VAR = 'ma valeur'
    }
    parameters {
        string(name: 'NAME', defaultValue: 'M. Jenkins', description: 'QuiEst ce ?')
        text(name: 'TEXT', defaultValue: 'un text', description: 'une description')
        booleanParam(name:'TOGGLE', defaultValue: true, description: 'true or false')
        choice(name:'CHOICE', choices: ['un','deux','trois'], description: 'liste')
        password(name: 'PASSWORD', description: 'un mode passe')
    }

    stages {

        stage('build'){

            steps{

                echo "NAME: ${ NAME }"
                echo "TEXT: ${ TEXT }"
                echo "TOGGLE: ${ TOGGLE }"
                echo "PASSWORD: ${ PASSWORD }"
                echo "MY_VAR: ${ env.MY_VAR}"
      
            }
        }
    }


}