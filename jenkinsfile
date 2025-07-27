node {
    stage('Start Orchestration') {
        echo "Starting central deployment pipeline..."
    }

    stage('Build & Deploy User Service') {
        echo "Triggering user-service pipeline..."
        build job: 'user-app'
    }

    stage('Build & Deploy Product Service') {
        echo "Triggering product-service pipeline..."
        build job: 'product-app'
    }

    stage('Build & Deploy Order Service') {
        echo "Triggering order-service pipeline..."
        build job: 'order-job'
    }

    stage('Complete') {
        echo "All services deployed successfully!"
    }
}
