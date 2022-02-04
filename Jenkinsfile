
pipeline {
    agent { label 'Ahmed-EC2' }

    stages {
        
        stage('Pukking Repo Files') {
            steps {
              git branch: "${GIT_BRANCH}",  url: 'https://github.com/ahmedKhaled1995/simple_nodejs_app'
            }
        }
        
         stage('build-Dockerfile') {
            steps {
                sh '''
                docker build -t 3omda-image .
                echo "Done ya 3omda"
                '''
            }
         stage('deploy') {
            steps {
                sh '''
                docker run 3omda-image 
                echo "Done ya 3omda"
                '''
            }
        }
        
    }
}
