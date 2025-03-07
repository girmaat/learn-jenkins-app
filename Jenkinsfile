pipeline {
    agent any

    stages {
<<<<<<< HEAD
        stage('Hello') {
            steps {
                echo 'Hello World'
=======
        stage('Build') {
            agent{
                docker{
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps {
                sh '''
                    ls -la
                    node --version
                    npm --version
                    npm ci
                    npm run build
                    ls -la
                '''
            }
        }
        stage('Test'){
              agent{
                docker{
                    image 'node:18-alpine'
                    reuseNode true
                }
            }
            steps{
                sh '''
                test -f build/index.html
                test -f src/app.js
                npm test
                '''
>>>>>>> d8104101cda68e74169d1d741b1e9cc516b37d36
            }
        }
    }
}
