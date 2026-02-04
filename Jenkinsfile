pipeline{
    agent any

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