properties([pipelineTriggers([pollSCM('30 * * * *')])])
node {
    stage("clone"){
    checkout([$class: 'GitSCM', branches: [[name: '*/main']], extensions: [], userRemoteConfigs: [[url: 'https://github.com/amichaizelig/MySoftware.git']]])    
    }
    stage("run python scripts"){
        bat "welcome.py"
        bat "click.py"
    }
}
