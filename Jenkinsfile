pipeline {
    agent any
    tools{
        maven "Maven3"
        jdk "jdk21"
        git "Default"
      }
        stages {
          stage ('check'){
            steps{
              git branch: 'main',
        url: 'https://github.com/Hoopsier/OTP-BS-OTHER.git' 'https://github.com/Hoopsier/OTP-BS-OTHER.git'
            }
        }
        stage ('build'){
            steps{
                sh 'mvn clean install'
            }
        }

        stage('test') {
            steps{
                sh 'mvn test'
            }
        }
        stage('jacoco'){
            steps{
                jacoco()
            }
        }

    }
}
