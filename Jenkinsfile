pipeline {
    agent any
    triggers {
        pollSCM '* * * * *'
    }
    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "M2_HOME"
        jdk "JAVA_HOME"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git 'https://github.com/ankitasthana-hu/hello-world.git'

                // Run Maven on a Unix agent.
                sh "mvn -Dmaven.test.failure.ignore=true clean package"

                // To run Maven on a Windows agent, use
                // bat "mvn -Dmaven.test.failure.ignore=true clean package"
            }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    
                    archiveArtifacts 'webapp/target/*.war'
                }
            }
        }
    }
}
