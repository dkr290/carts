pipeline{

    agent any


    tools{
       maven 'maven-3.6.3'
    }
   

    stages{
        stage('build'){
            steps{
                echo 'this is the compile job'
                sh 'mvn compile'
              
            }
        }
        stage('test'){
            steps{
                echo 'this is the test job'
                sh 'mvn clean test'
                
            }
        }
        stage('package'){
            steps{
                echo 'this is the package job'
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

