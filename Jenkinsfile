pipeline {
    agent {
        label 'Agent1'
    }

    environment { 
        COURSE = 'jenkins'
    }

    stages {
        stage('Build') {
            steps {
                script{
                    sh """
                        echo "Hello Build"
                        env                       
                    """
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

    post { 
        always { 
            echo 'I will always say Hello again!'
            // deleteDir()
        }
        success{
            echo 'Hello success'
        }
        failure{
            echo 'Hello failure'
        }
    }
}