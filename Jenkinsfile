// Allocate Build Node
node('master') {
    stage("Fetch Source Code") {
        git 'https://github.com/TrainingByPackt/Beginning-Continuous-Delivery-With-Jenkins'
    }

    dir('Lesson5') {
        printMessage('Running Pipeline')

        stage("Testing") {
            sh 'python test_functions.py'
        }

        printMessage('Pipeline Complete')
    }
    stage('Deploy') {
        if (env.BRANCH_NAME=='master') {
            printMessage('Master upload')
            else
                printMessage('Staging upload')
        }
    }
}

def printMessage(message) {
    echo "${message}"
}
