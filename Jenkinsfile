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
        stage ('MVN SONARQUBE') {
            steps {
                sh 'mvn clean compile'
            }
        }
        stage ('Compile') {
            steps {
                sh 'mvn sonar:sonar -Dsonar.login=squ_9a19fde0f779d634c24c81f75f48a75d8107519f -Dmaven.test.skip=true"
            }
        }
        
    }
    
}
