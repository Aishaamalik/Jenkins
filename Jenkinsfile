pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'python3 hello.py'
                sh 'gcloud compute zones list'
                sh 'gcloud compute scp /var/lib/jenkins/workspace/abc_main/*.html root@ashyellow-apache:/var/www/html --zone=us-west4-b'
            }
        }
    }
}
