pipeline{
    agent any
    tools{
        maven 'maven-v3'
    }
    stages{
        stage("checkout"){
            steps{
                git url:"https://github.com/mindwisetech/spring-application.git", branch:"main"
            }
        }
        stage("compile"){
            steps{
                sh "mvn compile"
            }
        }
        stage("test"){
            steps{
                sh "mvn test"
            }
        }
        stage("package"){
            steps{
                sh "mvn package"
            }
        }
        stage("Run"){
            steps{
                sh "java -jar target/spring-petclinic-3.5.0-SNAPSHOT.jar"
            }
        }
    }
}
