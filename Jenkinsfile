node('master') {

    currentBuild.result = "SUCCESS"

    try {

       stage('Checkout'){

          checkout scm
       }

       stage('build'){

       }

       stage('Test Security'){

       }

       stage('Cleanup'){

       }


    }
    catch (err) {

        currentBuild.result = "FAILURE"

        throw err
    }

}