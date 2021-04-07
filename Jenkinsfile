pipeline{
    agent any
    tools{
        jdk 'JDK_8'
        gradle 'GRADLE'
    }
    stages{
        
        stage('sonar analysis') {
                steps {
                
                sh 'gradle sonarqube -Dsonar.host.url=http://localhost:9000 -Dsonar.login=574af6ac5de7c5fcc6ace6ab57a3c028e35897e5 -Dsonar.verbose=true'  
            }
        }
        
        /*stage('Compile') {
          steps {
            // Compile the app and its dependencies
            sh './gradlew compileDebugSources'
          }
        }*/
        stage('JunitTest') {
          steps {
            sh 'gradle clean test'
          }
        }
        stage('apk') {
          steps {
            sh 'gradle assemble'
          }
        }
        stage('Build') {
                steps {
                
                sh './gradlew build'  
            }
        }
    }
}
