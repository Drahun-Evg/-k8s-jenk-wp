pipeline {
    agent { label 'ubuntu-node-1' }
    stages {
        stage('test start minikube'){
            steps {
                sh 'echo ----------- START Deploy ----------'
                sh 'echo minikube start'
                sh 'minikube version'
                sh 'kubectl version --client'
                sh 'kubectl apply -k ./'
                sh 'minikube service wordpress --url'
                sh 'kubectl get deploy'
                sh 'echo ------------ END Deploy -----------'
            }
        }
    }
}
