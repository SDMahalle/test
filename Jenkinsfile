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
stage('Update POM') {
                            steps {
                                sh '''
                                    # Clone the test2 repository
                                     echo "repo cloning started"
                                    git clone https://github.com/SDMahalle/test3.git
                                    cd test3
                                    echo "navigated to test 3"
                                    # Checkout the main branch
                                    git checkout main
                                    echo "checked out main branch"
                                    # Make changes to the pom.xml file
                                    # (Assuming you have a script or command to update the pom.xml)
                                    # For example, using sed to update a version number
                                    sed -i 's/<version>1.0-SNAPSHOT</version>/<version>1.1-SNAPSHOT</version>/' pom.xml
                                    echo "updated pom version"
                                    # Commit and push the changes
                                   # git config user.name "your-username"
                                   # git config user.email "your-email@example.com"
                                    git add pom.xml
                                    git commit -m "Update pom.xml version"
                                    echo "commit updated pom.xml"
                                    git push origin main
                                    echo "push updated pom.xml"
                                '''
                            }
                        }
    }
}