pipeline {
    agent any 
triggers { pollSCM:('* * * * *')}
tools {
     jdk 'jdk-17'
     maven mvn-3.9.12
  }
parameters {choices(name:'CHOICES',choices:['mvn validate','mvn package','mvn clean','mvn test'])
  }
    stages {
         stage ('git clone') {
           steps {
               git branch: 'main',
                  url:'https://github.com/kasagonirithish/spring-petclinic.git'
             }
         }
         stage ('mvn package') {
           steps {
                echo "choice: ${CHOICES}"
         }
     }

  }