pipeline {
    agent {
        docker {
            image 'maven' 
            args '-v $HOME/.m2:/root/.m2'
            args '-u root'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -X -B -s mule-settings-jenkins.xml -DskipTests -Dhttp.proxyHost=proxy.det.nsw.edu.au -Dhttp.proxyPort=80 -Dhttps.proxyHost=proxy.det.nsw.edu.au -Dhttps.proxyPort=80 clean package' 
            }
        }
    }
}
