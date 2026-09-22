pipeline {
    agent any
    tools{
        maven "Maven3"
        jdk "jdk21"
      }
        stages {
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
