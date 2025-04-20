pipeline {
    agent any

    tools{
      maven 'Maven 3.9.9'
    }
  
    stages {
        stage('One') {
            steps {
                echo 'Compiling'
                sh 'mvn compile'
            }
        }
        stage('Two') {
            steps {
                echo 'Testing'
                sh 'mvn clean tests'
            }
        }
        stage('Three') {
            steps {
                echo 'Packaging'
                sh 'mvn package -DskipTests'
            }
        }
    }
  post{
    always{
      echo 'Completed'
    }
  }
}
