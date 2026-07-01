pipeline {
    agent any
    stages {
        stage('git clone') {
          steps {
            git branch: 'main',url: 'https://github.com/kasagonirithish/spring-petclinic.git'
          }
        }
        stage('validate') {
            steps {
                 sh 'mvn --version'
                 sh 'mvn validate'
            }
        }
    }
}
    