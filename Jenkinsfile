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
         mail bcc: '', body: 'adding email test', cc: '', from: '', replyTo: '', subject: 'job status', to: 'akshyanshal@gmail.com'
        }
    }
    stage('added modified file'){
        steps{
            git 'https://github.com/Akshyanshalenka/onlinebookstore.git'
        }
    }
}
}
