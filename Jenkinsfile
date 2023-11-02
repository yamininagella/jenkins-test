pipeline {
    agent any
    stages {
        stage("xyz"){
            steps { 
                echo geturl()
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
