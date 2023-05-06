pipeline {
     agent any
     tools (nodejs "node")
     stages {
        stage("Build") {
            steps {
                h '${WORKSPACE}/jenkins/pipeline/update-jenkins-plugins-ppln/update-plugins.sh'
                sh "npm install"
                sh "npm run build"
            }
        }
        // stage("Deploy") {
        //     steps {
        //         sh "sudo rm -rf /var/www/jenkins-react-app"
        //         sh "sudo cp -r ${WORKSPACE}/build/ /var/www/jenkins-react-app/"
        //     }
        // }
    }
}