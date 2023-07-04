
pipeline { 
    agent any  
    options {
        timeout(time: 1, unit: 'HOURS')
        disableConcurrentBuilds()
        buildDiscarder(logRotator(numToKeepStr: '10'))
        timestamps()
    }
    triggers {
        //pollSCM(env.GIT_BRANCH == main_branch ? '* * * * *': 'H/15 * * * *' )
        pollSCM('* * * * *')
    }

    stages { 
        stage('Build') { 
            steps { 
               echo 'This is a minimal pipeline.' 
            }
        }
    }
}