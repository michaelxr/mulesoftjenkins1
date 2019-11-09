pipeline {
    agent {
        docker {
            image 'maven' 
            args '-u michaelrobinson'
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
