pipeline {
    agent {
        docker {
            image 'maven' 
            args '-v $HOME/.m2:/root/.m2'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -s mule-settings-jenkins.xml -DskipTests clean package' 
            }
        }
    }
}
