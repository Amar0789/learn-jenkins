pipeline{
    agent any
    stages{
        stage('one'){
            steps{
                echo "Hi I am from one"
            }
        }
        stage('Two'){
            steps{
                echo "Hi I am from Two"
            }
        }
        stage('Three'){
            steps{
                echo "Hi I am from Three"
            }
        }
        stage('Four'){
            steps{
                echo "Hi I am from Four"
            }
        }
        stage('Five'){
            steps{
                echo "Hi I am from Five"
            }
        }
    post{
        always{
            echo 'THis is from always'
        }

        success{
            echo 'This gets executed when only script gets succeeded'
        }
    }
    }
}