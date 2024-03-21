pipeline{
    agent any
    environment{
        NEW_VERSION = '0.0.1'
    }
    parameters{
        choice(name:'VERSION' , choices: ['1.1.0', '1.2.0', '1.3.0'], description: '')
        booleanParam(name: 'executeTests', defaultValue: true, description: '')
    }

    stages {
        stage('checkout') {
            steps {
                echo 'checkout stage'
            }
        }
        stage('build') {
            steps {
                echo 'build stage'
                echo " building version ${NEW_VERSION}"
            }
        }
        stage('test') {
            steps {
                echo 'test stage'
                //echo 'test server credentials ${server-credentials}'
            }
        }
        stage('quality-check') {
            steps {
                echo 'quality assurance stage'
            }
        }
        stage('deploy') {
            steps {
                echo 'deployment stage'
                echo 'deploying version ${params.VERSION}'
                echo 'deploying description: ${params.description}-ticket'
            }
        }
  }
}
