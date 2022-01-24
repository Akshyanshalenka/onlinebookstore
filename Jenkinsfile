pipeline {
    agent any

    tools {
        // Install the Maven version configured as "M3" and add it to the path.
        maven "mvn"
    }

    stages {
        stage('Build') {
            steps {
             
                // Run Maven on a Unix agent.
                sh "mvn  clean package"
        }
    }
    stage('Test')
    {
        steps{
            echo "Testing start App"
        }
    }
    stage('email notification'){
        steps {
            mail bcc: '', body: 'sample email for testing', cc: '', from: '', replyTo: '', subject: 'job status', to: 'akshyanshal@gmail.com'
        }
    }
    stage('git checkout'){
        setps{
            https:'//github.com/Akshyanshalenka/GitJava.git'
        }
    }
}
}
