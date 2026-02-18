stage('Build Images') {
    steps {
        sh 'docker build -t eureka-server:latest ./eureka-server'
        sh 'docker build -t api-gateway:latest ./api-gateway'
        sh 'docker build -t user-service:latest ./user-service'
        sh 'docker build -t movie-service:latest ./movie-service'
        sh 'docker build -t email-service:latest ./email-service'
        sh 'docker build -t cinevision-frontend:latest ./frontend'
    }
}

stage('Deploy to Kubernetes') {
    steps {
        sh 'kubectl apply -f k8s/'
    }
}
