pipeline {
    agent any
 parameters {
            string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Branch to build')
        }
    stages {
        stage('Build') {
            steps {
                sh 'echo "Hello World"'
                sh '''
                    echo "Multiline shell steps works too"
                    ls -lah
                '''
            }
        }
 stage('Release') {
                    steps {
                        sh 'echo "Hello World Release"'
                        sh '''
                            echo "Multiline shell steps works too"
                            ls -lah
                        '''
                    }
                }
    }
}