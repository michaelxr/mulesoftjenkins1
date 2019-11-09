pipeline {
    agent {
        docker {
            image 'maven' 
            arg '-u michaelrobinson'
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