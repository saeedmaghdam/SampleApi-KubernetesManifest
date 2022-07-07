pipeline {
    agent any
    stages {
        stage('Update Git') {
            steps {
                sh 'pwd'
                sh 'git config user.email smasafat@gmail.com'
                sh 'git config user.name saeedmaghdam'
                sh 'sed -i "s+saeedmaghdam/sample-api.*+saeedmaghdam/sample-api:${DOCKERTAG}+g" deployment.yaml'
                sh 'git add .'
                sh 'git commit -m "Done by Jenkins Job changemanifest: $DOCKERTAG"'
                sh 'git push origin HEAD:main'
            }
        }
    }
}