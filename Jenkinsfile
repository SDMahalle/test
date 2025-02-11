pipeline {
    agent any
  parameters {
        string(name: 'BRANCH_NAME', defaultValue: 'main', description: 'Branch to build')
        choice(name: 'BUILD_TYPE', choices: ['Snapshot', 'Release'], description: 'Choose build type')
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