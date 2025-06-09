pipeline { 
    agent any 
    tools { 
        maven 'Maven'  
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'main', url: 'https://github.com/lastbench26/lab01.git'  
            } 
        } 
        stage('Build') {  
            steps { 
                bat 'mvn clean package'  
            } 
        } 
        stage('Test') {  
            steps { 
                bat 'mvn test'  
            } 
        } 
        stage('Run Application') {  
            steps { 
                bat 'java -jar target/lab01-0.0.1-SNAPSHOT.jar'  
            } 
        } 
    } 
}
