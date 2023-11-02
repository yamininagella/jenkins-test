pipeline {
    agent any
    stages {
        stage("getUrl"){
            steps { 
                echo getUrl()
            }
        }
        stage("getUrlName"){
            steps { 
                echo getUrlName()
            }
        }
        stage("getUrlNameE"){
            steps { 
                echo getUrlNameE()
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


def getUrl(){
 return scm.getUserRemoteConfigs()[0].getUrl()   
}

def getUrlName(){
 return scm.getUserRemoteConfigs()[0].getUrl().tokenize("/")[-1].tokenize(".")[0] 
}

def getUrlNameE(){
 return scm.getUserRemoteConfigs()[0].getUrl().tokenize("/")[3].split("\\.")[0] 
}
