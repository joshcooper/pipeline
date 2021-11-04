pipeline {
    agent any

    parameters {
        string(name: 'SHA', description: 'blah')
    }
    stages {
        stage('Build') {
            matrix {
                axes {
                    axis {
                        name 'PLATFORM'
                        values 'a', 'b'
                    }
                }
                stages {
                    stage('Building') {
                        steps {
                            echo "building ${PLATFORM}"
                        }
                    }
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
