node('master') {

    currentBuild.result = "SUCCESS"

    try {

       stage('Checkout'){
            checkout scm
       }

       stage('build'){
            sh 'curl -Os https://nodejs.org/dist/v6.3.0/node-v6.3.0-linux-x64.tar.gz'
            sh 'tar xvfz node-v6.3.0-linux-x64.tar.gz >tar_explode.log'
            sh 'npm install'
            sh 'npm install --save --dev retire'
       }

       stage('Test Security'){
            sh 'node_modules/.bin/retire'
       }

       stage('Cleanup'){

       }


    }
    catch (err) {

        currentBuild.result = "FAILURE"

        throw err
    }

}