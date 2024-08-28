node {
    stage('Download code from SCM') {
    git branch: 'dev', url: 'https://github.com/venkat9822891/maven-working-code.git'
                                    }
    stage('Convert into artifacts') {
    sh 'mvn package'
                                    }
    stage('deployment ') {
    deploy adapters: [tomcat9(credentialsId: '604b220d-d9a8-4dc1-9b70-c257f5c45eb1', path: '', url: 'http://172.31.41.18:8080')], contextPath: '/dev-app', war: '**/*.war'
}
}
