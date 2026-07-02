pipeline {
    agent any
    triggers { pollSCM('* * * * *')}
    tools{    
        jdk   'jdk-17'
        maven 'mvn-3.9.12'
    parameters { choice:(name:'CHOICES', choices:['mvn package','mvn clean','mvn test','mvn validate'])
    stages {
        stage('git clone') {
            steps {
                git branch: 'main'
                    url:'https://github.com/kasagonirithish/spring-petclinic.git'
        stage('maven build') {
            steps {
                echo "choice: ${params.CHOICES}"
            }
        }            
            }
        }
    }
    ]
    } 
    }
    
    }
