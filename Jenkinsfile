node('php'){
    stage('Clean'){
        deleteDir()
        sh 'ls -la'
    }
    
    stage('Fetch') {
        checkout scm
    }
    
    stage('Docker Build') {
        sh 'docker build -t brunormr80/laravel:$BUILD_NUMBER .'
    }
    
    stage('Docker Ship') {
        sh 'docker push brunormr80/laravel:$BUILD_NUMBER'
    }
}
