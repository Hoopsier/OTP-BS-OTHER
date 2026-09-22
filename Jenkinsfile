pipeline {
    agent any
        stages {
        stage ('check'){
            steps{
                git 'https://github.com/Hoopsier/OTP-BS-OTHER.git'
            }
        }
        stage ('build'){
            steps{
                bat 'mvn clean install'
            }
        }

        stage('test') {
            steps{
                bat 'mvn test'
            }
        }
        stage('jacoco'){
            steps{
                jacoco()
            }
        }

    }
}
