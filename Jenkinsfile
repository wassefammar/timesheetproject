pipeline{

    agent any 
    tools{
        maven 'M2_HOME'
    }
    stages {
        stage ('GIT') {
            steps {
                git branch : 'master',
                url: 'https://github.com/wassefammar/timesheetproject.git'
            }
        }
        stage ('Compile') {
            steps {
                sh 'mvn clean compile'
            }
        }
        
    }
    
}
