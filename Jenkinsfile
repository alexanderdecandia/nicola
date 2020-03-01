 stage('DeployToProduction') {
            when {
                branch 'master'
            }
            steps {
                input 'Deploy to Production?'
                milestone(1)
                kubernetesDeploy(
                    kubeconfigId: 'kubeconfig',
                    #configs: 'mysql-deployment.yaml',
                    configs: 'wordpress-deployment.yaml',
                    enableConfigSubstitution: true
                )
            }
        }
    }
}
