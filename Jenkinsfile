pipeline{
    agent any

    options {
        retry(3)
        disableConcurrentBuilds()
        timeout(time:'10', unit:'MINUTES')
        timestamps()
        ansicolour('xterm')
    }

    environment{
        envv = 'prod not'
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