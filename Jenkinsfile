pipeline {
    agent {
        docker {
            image 'maven' 
            args '-u root'
        }
    }
    stages {
        stage('Build') { 
            steps {
                sh 'mvn -B -DskipTests -Dhttp.proxyHost=proxy.det.nsw.edu.au -Dhttp.proxyPort=80 -Dhttp.nonProxyHosts=localhost|127.0.0.1  -Dhttps.proxyHost=proxy.det.nsw.edu.au -Dhttps.proxyPort=80 -Dhttps.nonProxyHosts=localhost|127.0.0.1 clean package' 
            }
        }
    }
}
