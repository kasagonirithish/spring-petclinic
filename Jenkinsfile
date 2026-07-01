pipeline {
    agent any
    triggers { pollSCM('* * * * *') } 
    parameters {choice(name: 'CHOICES', choices: ['mvn validate','mvn package','mvn clean','mvn test'])
    }
    stages {
        stage('git clone') {
          steps {
            git branch: 'main',url: 'https://github.com/kasagonirithish/spring-petclinic.git'
          }
        }
        stage('validate') {
            steps {
                 echo "choice: ${params.CHOICES}"
            }
        }
    }
}
    