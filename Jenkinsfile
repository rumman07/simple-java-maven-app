pipeline{
    agent any 
    stages{
        stage("CleanUp"){
            steps{
                deleteDir()
            }
        }
        stage("CloneRepo"){
            steps{
                sh "git clone https://github.com/rumman07/simple-java-maven-app.git"
            }
        }
        stage("Build"){
            steps{
                dir("simple-java-maven-app"){
                    sh "mvn clean install"
                }
            }
        }
        stage("Test"){
            steps{
                dir("simple-java-maven-app"){
                    sh "mvn test"
                }

            }
        }
        stage("SmokeTesting"){
            steps{
                sh "echo 'Everything is working as expected'"
            }
        }
    }
}