node('slave2') {
    stage('Clone Repo') {
        git branch: 'prod', credentialsId: 'jenkins_agent', url: 'git@github.com:DhivakarKS31/devops.git'
    }
    stage('Build') {
       sh  "sudo cp index.html /var/www/html/index.html"
    }
    stage("Clean Workspace"){
            cleanWs cleanWhenAborted: true, cleanWhenFailure: true, cleanWhenNotBuilt: true, cleanWhenUnstable: true, notFailBuild: true
    }
}
