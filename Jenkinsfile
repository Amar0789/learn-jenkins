pipeline{
    agent any

    options {
        retry(3)
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
        choice(name: 'Env Type', choices ['PROD','DEV','QA'], description:'PLease select env')
    }
    stages{
        stage('one'){
            steps{
                echo "From ${version}"
            }
        }
        stage('Two'){
            steps{
                echo "From ${envv}"
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