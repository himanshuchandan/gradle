pipeline{
    agent any
    tools{
        jdk 'JDK_8'
        gradle 'GRADLE'
    }
    stages{
        /*
        stage('sonar analysis') {
                steps {
                
                sh 'mvn -f /var/lib/jenkins/workspace/student_data_101/bootjpa/pom.xml clean install sonar:sonar'  
            }
        }
        */
        stage('Build') {
                steps {
                
                sh './gradlew build'  
            }
        }
    }
}
