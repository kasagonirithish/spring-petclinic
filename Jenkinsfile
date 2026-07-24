pipeline {
    agent {
      label 'spc-node'
    }
triggers { pollSCM('0 0 * * *')}
tools {
    jdk 'jdk-17'
    maven 'mvn-3.9.12'
}  
parameters {
   choice(name: 'GOALS',choices:['mvn package','mvn validate','mvn test','mvn clean'])
}
stages {
    stage('git clone') {
        steps {
            git branch: 'main',
               url: 'https://github.com/kasagonirithish/spring-petclinic.git'
        }
    }
    stage('mvn build') {
         steps {
            sh "${params.GOALS}"
         }
    } 
}
} 