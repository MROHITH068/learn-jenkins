pipeline {
    agent {node {label 'workstation'}}

    environment {
    SSH = credentials('SSH')
    }

    options{
    ansicolor('xterm')
    }
    stages {
        stage('Hello') {
            steps {
                echo 'Hello World'
                sh 'env'
            }
        }
    }
    post{
        always{
        sh 'echo Post'
        }
    }
}
