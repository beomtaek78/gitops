pipeline {
    agent any
    stages {
        stage('git pull') {
            steps {
                git url: 'https://github.com/beomtaek78/gitops.git', branch: 'main'
            }
        }
        stage('k8s deploy'){
            steps {
                kubernetesDeploy(kubeconfigId: 'kubeconfig', configs: '*.yaml')
            }
        } 
    }
}
