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
    }
    stages{
        stage('one'){
            steps{
                echo "From one"
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