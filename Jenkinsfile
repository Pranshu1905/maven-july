pipeline{
    
    agent any  // here any = current available ec2 server where jenkins is installed
    
    tools{
        maven 'maven-3.8.7'
    
    }
    
    stages{
        
        stage('Checkout Code')
        {
            steps{
                git 'https://github.com/Pranshu1905/maven-july.git'
            }
        }
        stage('Compile Code'){
            steps{
                echo "compiling the code...."
                sh 'mvn compile'
            }
        }
        stage('Test code'){
            steps{
                echo "testing the code using maven surefire"
                sh 'mvn test'
            }
        }
        
        stage('BuildCode'){
            steps{
                echo "generating artifact..."
                sh 'mvn package'
            }
        }
        
    }
    
    
    
}
