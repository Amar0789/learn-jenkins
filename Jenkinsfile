pipeline{
    agent any

    stages{
        stage('one'){
            steps{
                echo "From one"
            }
        }
        stage('Two'){
            steps{
                echo "From Two"
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