pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "Maven3"
    }

    stages {
        stage('Build') {
            steps {
                // Get some code from a GitHub repository
                git url: 'https://github.com/Javacream/org.javacream.training.cicd.git', branch: 'audi_29.1.2024'
                echo 'Done clone'
                // Run Maven on a Unix agent.
                dir('projects'){
                    sh "mvn -Dmaven.test.failure.ignore=true clean package"
                }
        }

            post {
                // If Maven was able to run the tests, even if some of the test
                // failed, record the test results and archive the jar file.
                success {
                    junit '**/target/surefire-reports/TEST-*.xml'
                    archiveArtifacts '**/target/*.jar'
                }
            }
        }
    }
}
