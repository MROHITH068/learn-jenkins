pipeline {
    agent {node {label 'workstation'}}

    environment {
    SSH = credentials('SSH')
    }

    options{
    ansiColor('xterm')
    }

    parameters{
        string(name:'APP_INPUT', defaultValue:'', description:'Just Input')
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'env'
                sh 'echo APP_INPUT:- $APP_INPUT'
            }
        }
    }
    post{
        always{
        sh 'echo Post'
        }
    }
}
