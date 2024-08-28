node {
    stage('Download code from SCM') {
    git branch: 'dev', url: 'https://github.com/venkat9822891/maven-working-code.git'
                                    }
    stage('Convert into artifacts') {
    sh 'mvn package'
                                    }
    stage('deployment ') {
    deploy adapters: [tomcat9(credentialsId: '46bb79ce-0171-488c-a847-6b86816dbb83', path: '', url: 'http://172.31.35.198:8080')], contextPath: '/test-app', war: '**/*.war'
}
}
