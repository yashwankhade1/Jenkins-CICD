stage('Build on kubernetes'){
        steps {
            withKubeConfig([credentialsId: 'kubeconfig']) {
                sh 'pwd'
                sh 'cp -R helm/* .'
                sh 'ls -ltrh'
                sh 'pwd'
                sh '/usr/local/bin/helm upgrade --install petclinic-app petclinic --set image.repository=iamsakib/petclinic --set image.tag=${BUILD_NUMBER}'
        }
    }
}




}

}
