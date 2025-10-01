pipeline{

    agent any

    tools{
       maven 'Maven3.9.11' 
    }
 
    stages{
        stage('build'){
            steps{
                echo 'compiling sysfoo app...'
                sh 'mvn compile'
            }
        }
        stage('test'){
            steps{
                echo 'running unit tests...'
                sh 'mvn clean test'
            }
        }
        stage('package'){
            steps{
                echo 'packaging the app....'
                sh 'mvn package -DskipTests'
            }
        }
    }
    
    post{
        always{
            echo 'this pipeline has completed...'
        }
        
    }
    
}
