pipeline{

agent any 

stages{
    stage('First Stgae'){
        steps{
          checkout scmGit(branches: [[name: '*/main'], [name: '*/test']],
            extensions: [], 
            userRemoteConfigs: [[url: 'https://github.com/vikasaroor/ITDefined_Prac.git']])
        }
    } 
    stage('Second Stgae'){
        steps{
            echo 'Hello In Second'
        }
    } 


}
}