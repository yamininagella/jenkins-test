pipeline {
    agent any
    stages {
        stage("xyz"){
            steps {
                xyz = geturl()
                echo "$xyz"
            }
        }
    }
    post { 
        cleanup {
            cleanWs()
            echo 'cleanup workspace'
        }
    }
}


def geturl(){
 return scm.getUserRemoteConfigs()[0].getUrl()   
}
