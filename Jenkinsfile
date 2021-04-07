pipeline{
    agent any
    tools{
        jdk 'JDK_8'
        gradle 'GRADLE'
    }
    stages{
        
        stage('sonar analysis') {
                steps {
                
                sh 'gradle sonarqube -Dsonar.host.url=http://localhost:9000 -Dsonar.verbose=true'  
            }
        }
        
        /*stage('Compile') {
          steps {
            // Compile the app and its dependencies
            sh './gradlew compileDebugSources'
          }
        }*/
        stage('Build') {
                steps {
                
                sh './gradlew build'  
            }
        }
    }
}
