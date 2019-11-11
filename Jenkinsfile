pipeline {
    agent {
        docker {
            image 'maven' 
            arg '-u root'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests clean package' 
            }
        }
    }
}
