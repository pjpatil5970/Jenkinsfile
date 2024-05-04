pipeline {
    agent any
    stages {
        stage('BUILD') {
            steps {
                echo 'This is Build stage'
                sh '''
        sleep 5
            exit 0
       '''
            }
        }

        stage('TEST PARALLEL') {
            parallel {
                stage('Test on chrome') {
                    steps {
                        echo 'This is Test on chrome browser'
                        sh 'sleep 5; exit 0'
                    }
                }
                stage('Test on safari') {
                    steps {
                        echo 'This is Test on safari browser'
                        sh 'sleep 5; exit 0'
                    }
                }
            }
        }
        stage('DEPLOY') {
            parallel {
                stage('Server1') {
                    steps {
                        echo 'This is Deploy to server1'
                        sh 'sleep 5'
                    }
                }
                stage('Server2') {
                    steps {
                        echo 'This is Deploy to server2'
                        sh 'sleep 5'
                    }
                }
                stage('Server3') {
                    steps {
                        echo 'This is Deploy to server3'
                        sh 'sleep 5'
                    }
                }
                stage('Server4') {
                    steps {
                        echo 'This is Deploy to server4'
                        sh 'sleep 5'
                    }
                }

            }
        }
    }
}
