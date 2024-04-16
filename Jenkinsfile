pipeline {
    agent any
    stages {
        stage("Build") {
            steps {
                echo "Building..."
            }
            post {
                success {
                    echo "Build Successful!"
                    mail to: "${EMAIL_DESTINATION}",
                    subject: "Build Status Email",
                    body: "Build was successful!"
                }
            }
        }
    }
}