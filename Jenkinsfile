Creating a Job 
 
Dashboard, Add new Item, name, Pipeline project 
OK 
Pipeline script from SCM (Source Code Management) 
Note down script box Jenkinsfile(To be created in Github repository) 
 
pipeline { 
    agent any 
    tools { 
          maven ' Maven' //Ensure name matches with configured  
    } 
    stages { 
        stage('Checkout') {  
            steps { 
                git branch: 'master', url: 'https://github.com/Naveen-Ka31/h.git'  
            } 
    } 
     stage('Build') {  
            steps { 
                sh 'mvn clean package'  
            } 
      } 
     stage('Test') {  
            steps { 
                sh 'mvn test'  
            } 
      } 
     stage('Run Application') {  
            steps { 
                sh 'java –jar target/Hello2-0.0.1-SNAPSHOT.jar'  
            } 
      } 
    } 
}
