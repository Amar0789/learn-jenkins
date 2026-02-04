pipeline{
    agent any

    options {
        retry(1)
        disableConcurrentBuilds()
        timestamps()
        timeout(time: 10, unit:'SECONDS')
        ansiColor('xterm')
    }
    environment{
        envv = 'prod not'
    }

    parameters {
        string(name: 'version', defaultValue: '1.0.0', description: 'This is the version of the build')
        choice(name: 'Env Type', choices: ['PROD','DEV','QA'], description: 'PLease select env')
        booleanParam(name: 'deploy', defaultValue: 'FALSE')
        text(name: 'Name', defaultValue: 'ex:stephen', description: 'Enter your username')
        password(name: 'USER PASSWORD', defaultValue: '')
    }
    stages{
        stage('one'){
            steps{
                echo "From ${version}"
            }
        }
        stage('Two'){
            steps{
                echo 'pipeline failure'
            }
        }
        stage('Approval') {
            steps {
                input message: 'Proceed to deploy?'
            }   
        }   
    }    
    post{
        always{
            echo "It runs always"
        }
        success{
            echo "It runs when succeeded"
        }
    }
}